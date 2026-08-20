# X API Integration (via curl)

How FARTBULL agents interact with X (formerly Twitter) using curl-based shell helpers, inspired by the original `xurl-helpers` package.

## Overview

Agents can post tweets, reply to mentions, and interact with the X API entirely through shell commands using curl. This enables autonomous agents to engage on social platforms.

## Requirements

- X API key with `tweet.read`, `tweet.write`, `users.read`, `offline.access` scopes
- `curl`, `jq`, and standard Unix tools
- Environment variable: `X_BEARER_TOKEN` (TODO: verify exact format)

TODO: Verify exact API endpoint URLs and token format from `https://developer.x.com/en/docs/twitter-api`

## Posting a Tweet

```bash
# Simple post
post_tweet() {
  local text="$1"
  local url="https://api.twitter.com/2/tweets"
  
  curl -sf -X POST "$url" \
    -H "Authorization: Bearer $X_BEARER_TOKEN" \
    -H "Content-Type: application/json" \
    -d "{\"text\": \"$text\"}"
}

# Usage
post_tweet "Hello from FARTBULL agent!"
```

## Replying to a Tweet

```bash
reply_to_tweet() {
  local text="$1"
  local in_reply_to_id="$2"
  local url="https://api.twitter.com/2/tweets"
  
  curl -sf -X POST "$url" \
    -H "Authorization: Bearer $X_BEARER_TOKEN" \
    -H "Content-Type: application/json" \
    -d "{\"text\": \"$text\", \"reply\": {\"in_reply_to_tweet_id\": \"$in_reply_to_id\"}}"
}

# Usage
reply_to_tweet "Thanks for the suggestion!" "1234567890123456789"
```

## Fetching Mentions

```bash
# Get recent mentions of the authenticated user
MY_USER_ID=$(curl -sf -X GET "https://api.twitter.com/2/me" \
  -H "Authorization: Bearer $X_BEARER_TOKEN" | jq -r '.data.id')

# Fetch mentions
curl -sf -X GET "https://api.twitter.com/2/users/$MY_USER_ID/mentions?max_results=5" \
  -H "Authorization: Bearer $X_BEARER_TOKEN" | jq '.data'
```

## Error Handling

```bash
post_tweet_safe() {
  local text="$1"
  local response
  local http_code
  
  response=$(curl -sf -w "\n%{http_code}" -X POST \
    "https://api.twitter.com/2/tweets" \
    -H "Authorization: Bearer $X_BEARER_TOKEN" \
    -H "Content-Type: application/json" \
    -d "{\"text\": \"$text\"}" 2>&1)
  
  http_code=$(echo "$response" | tail -1)
  
  if [ "$http_code" != "201" ] && [ "$http_code" != "200" ]; then
    echo "Error posting tweet: HTTP $http_code"
    echo "$response" | head -n -1 | jq '.' 2>/dev/null || echo "$response" | head -n -1
    return 1
  fi
  
  echo "$response" | head -n -1 | jq -r '.data.id'
  return 0
}
```

## Safety Considerations

- **Rate limits**: 300 posts per 3-hour window (TODO: verify)
- **Reply rules**: Always wait for engagement before auto-replying
- **Privacy**: Never expose API keys in logs
- **Content review**: Review tweets before posting

See [Safety Principles](../concepts/safety.md) for more.

## See Also

- [Social Media Automation](autonomous.md#6-multi-account-coordination)
- [Universal Prompts](../prompts/universal-prompts.md)
