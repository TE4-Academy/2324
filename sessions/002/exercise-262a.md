**Node.js Övning: Enkel CRUD Webbserver**

**Mål:** Skapa en webbserver som kan hantera CRUD-operationer för en lista av objekt (t.ex. böcker).

**1. Förberedelser**

   - Se till att du är i din `nodejs_webserver`-katalog.
   - Om du inte redan har gjort det, installera Express:
     ```bash
     npm install express --save
     ```

**2. Skapa en grundläggande server**

   Om du inte redan har en `server.js` från tidigare, följ stegen i den tidigare tutorialen för att sätta upp en.

**3. Skapa en "databas" med böcker**

   - Lägg till följande kod i början av `server.js` för att skapa en temporär databas:
     ```javascript
     let books = [
         { id: 1, title: "Harry Potter and the Sorcerer's Stone", author: "J.K. Rowling" },
         { id: 2, title: "The Hobbit", author: "J.R.R. Tolkien" }
     ];
     ```

**4. Implementera CRUD-operationer**

   - **Läs (Read) alla böcker:**
     ```javascript
     app.get('/books', (req, res) => {
         res.json(books);
     });
     ```

   - **Lägg till (Create) en ny bok:**
     (Anta att klienten skickar JSON-data för boken)
     ```javascript
     app.use(express.json()); // för att kunna läsa JSON-data från POST requests

     app.post('/books', (req, res) => {
         const book = {
             id: books.length + 1,
             title: req.body.title,
             author: req.body.author
         };
         books.push(book);
         res.json(book);
     });
     ```

   - **Uppdatera (Update) en befintlig bok:**
     ```javascript
     app.put('/books/:id', (req, res) => {
         const book = books.find(b => b.id === parseInt(req.params.id));
         if (!book) return res.status(404).send('Book not found.');

         book.title = req.body.title;
         book.author = req.body.author;
         res.json(book);
     });
     ```

   - **Ta bort (Delete) en bok:**
     ```javascript
     app.delete('/books/:id', (req, res) => {
         const bookIndex = books.findIndex(b => b.id === parseInt(req.params.id));
         if (bookIndex === -1) return res.status(404).send('Book not found.');

         const deletedBook = books.splice(bookIndex, 1);
         res.json(deletedBook);
     });
     ```

**5. Testa din server**

   - Starta din server med:
     ```bash
     node server.js
     ```

   - Använd en webbläsare, Postman, eller ett annat verktyg för att testa dina endpoints:
     - GET `/books` för att hämta alla böcker.
     - POST `/books` med JSON-data för att lägga till en ny bok.
     - PUT `/books/:id` med JSON-data för att uppdatera en bok.
     - DELETE `/books/:id` för att ta bort en bok.
