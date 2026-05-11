1. Difference between res.send() vs res.sendFile()...
   res.send() is for any kind of response (returning some data like JSON or a string)
   res.sendFile() is a convenient shortcut for files (image, a PDF, or an HTML page)

2. A realtive path like "public/index.html" ensures the file paths are always correct, no matter where you run the app from.

3. Adding third page

- Create public/menu.html
- Add a new route in server.js
  app.get('/menu', (req, res) => {res.sendFile(path.join(\_\_dirname, 'public/menu.html'))})

* Restart the server and visit http://localhost:3000/menu
