## Fördjupning kring Mongo DB
### med exempelkod


**Demonstration 3: Ansluta till en databas med MongoDB och Mongoose**

...

**3. Ansluta till MongoDB och skapa en modell**

   - Anslut till MongoDB i din `app.js`:
     ```javascript
     const mongoose = require('mongoose');

     mongoose.connect('mongodb://localhost:27017/mydatabase', { useNewUrlParser: true, useUnifiedTopology: true });
     ```

   - Skapa en enkel Mongoose-modell för en bok:
     ```javascript
     const bookSchema = new mongoose.Schema({
         title: String,
         author: String,
         published: Date
     });

     const Book = mongoose.model('Book', bookSchema);
     ```

   - **Demonstrera hur man lägger till en bok i databasen:**
     ```javascript
     const newBook = new Book({
         title: "The Great Gatsby",
         author: "F. Scott Fitzgerald",
         published: new Date('1925-04-10')
     });

     newBook.save((err, savedBook) => {
         if (err) console.error(err);
         else console.log('Book saved:', savedBook);
     });
     ```

   - **Demonstrera hur man hämtar alla böcker från databasen:**
     ```javascript
     Book.find({}, (err, books) => {
         if (err) console.error(err);
         else console.log('All books:', books);
     });
     ```

   - **Demonstrera hur man uppdaterar en bok i databasen:**
     ```javascript
     Book.findOneAndUpdate({ title: "The Great Gatsby" }, { author: "Francis Scott Fitzgerald" }, { new: true }, (err, updatedBook) => {
         if (err) console.error(err);
         else console.log('Updated book:', updatedBook);
     });
     ```

   - **Demonstrera hur man tar bort en bok från databasen:**
     ```javascript
     Book.findOneAndDelete({ title: "The Great Gatsby" }, (err) => {
         if (err) console.error(err);
         else console.log('Book deleted.');
     });
     ```
