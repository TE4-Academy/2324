**Stödresurser för Övningsuppgift: Skapa en webbaserad bokhandel med Node.js**

**Om du kör fast:**

1. **Problem med att sätta upp servern med Express**
   
   - **Tips:** Se till att du har importerat Express korrekt och att du har definierat och lyssnat på rätt port.
   - **Kodexempel:**
     ```javascript
     const express = require('express');
     const app = express();
     const PORT = 3000;

     app.get('/', (req, res) => {
         res.send('Hello, Express!');
     });

     app.listen(PORT, () => {
         console.log(`Server is running on http://localhost:${PORT}`);
     });
     ```

   - **Referensmaterial:** [Express Getting Started Guide](https://expressjs.com/en/starter/installing.html)

2. **Problem med att ansluta till MongoDB**

   - **Tips:** Se till att MongoDB är igång och att du använder rätt anslutningssträng.
   - **Kodexempel:**
     ```javascript
     const mongoose = require('mongoose');
     mongoose.connect('mongodb://localhost:27017/online_bookstore', { useNewUrlParser: true, useUnifiedTopology: true });
     ```

   - **Referensmaterial:** [Mongoose Quick Start Guide](https://mongoosejs.com/docs/index.html)

3. **Problem med att definiera eller använda Mongoose-modeller**

   - **Tips:** Se till att ditt schema är korrekt definierat och att du har skapat en modell baserat på det schemat.
   - **Kodexempel:**
     ```javascript
     const bookSchema = new mongoose.Schema({
         title: String,
         author: String,
         publishedDate: Date,
         price: Number,
         description: String
     });

     const Book = mongoose.model('Book', bookSchema);
     ```

   - **Referensmaterial:** [Mongoose Models Documentation](https://mongoosejs.com/docs/models.html)

4. **Problem med att skicka eller ta emot data**

   - **Tips:** Se till att du har konfigurerat din Express-app för att tolka JSON-data och att du skickar data i rätt format från klienten.
   - **Kodexempel:**
     ```javascript
     app.use(express.json());
     ```

   - **Referensmaterial:** [Express Middleware Documentation](https://expressjs.com/en/guide/using-middleware.html)

5. **Problem med att testa API:er med Postman**

   - **Tips:** Dubbelkolla dina förfrågningsmetoder (GET, POST, PUT, DELETE) och se till att du skickar rätt data i body-sektionen för POST- och PUT-förfrågningar.
   - **Kodexempel:** När du testar POST-routen i Postman, se till att du väljer "Body" -> "raw" -> "JSON (application/json)" och skickar data som:
     ```json
     {
       "title": "A Sample Book",
       "author": "Sample Author",
       "publishedDate": "2022-01-01",
       "price": 20,
       "description": "This is a sample book."
     }
     ```

   - **Referensmaterial:** [Postman Learning Center](https://learning.postman.com/)

