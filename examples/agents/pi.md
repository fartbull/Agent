# Pi Examples

> Pi is conversational only — no file system or shell access.

## Example 1: Code Explanation

```
You: Explain how the rate limiting works in src/middleware/rate_limit.py.
     I'm using Express.js and it uses a token bucket algorithm.
```

## Example 2: Architecture Discussion

```
You: I'm designing a payment system. Should I use a monolith or
     microservices? Consider scalability and team size.
```

## Example 3: Code Review (Paste Code)

```
You: Review this function for security issues:

     function getUser(id) {
       const query = 'SELECT * FROM users WHERE id = ' + id;
       return db.query(query);
     }
```
