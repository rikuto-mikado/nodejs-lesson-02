# Node.js Lesson 02

## What I Learned

- Handle POST request data streams with `req.on('data')` and `req.on('end')`
- Collect chunks into array and convert to string using `Buffer.concat(body).toString()`
- Parse form data (`message=value`) with `split('=')[1]`
- Save to file with `fs.writeFileSync()`
- Redirect with status code 302 and `Location` header

## Difficulties

- **Variable scope**: Used `chunk` before it was defined (needs to be inside callback)
- **Typo**: Mixed up `parseBody` and `parsedBody`
- **Async timing**: POST data isn't immediately available, must wait for `'end'` event

## How to Run

```bash
node app.js
```

Access `http://localhost:3000` in your browser
