# Tre demonstrationer från dagens lektion
## OBS: detta är bara referens från morgonen, inget du behöver göra

**Demonstration 1: Introduktion till Node.js och skapa en grundläggande server**

**1. Introduktion till Node.js**
   - Vad är Node.js?
   - Varför använda Node.js?
   - [Referenslänk](https://nodejs.org/en/about/)

**2. Installation av Node.js**
   - Gå till [Node.js officiella webbplats](https://nodejs.org/) och ladda ner den rekommenderade versionen.
   - Följ installationsanvisningarna för ditt operativsystem.
   - Verifiera installationen med kommandona:
     ```bash
     node -v
     npm -v
     ```

**3. Skapa din första server**
   - Initiera ett nytt projekt:
     ```bash
     mkdir first_server
     cd first_server
     npm init -y
     ```

   - Skriv en enkel server med inbyggda `http`-modulen. Skapa en fil `server.js`:
     ```javascript
     const http = require('http');

     const server = http.createServer((req, res) => {
         res.writeHead(200, { 'Content-Type': 'text/plain' });
         res.end('Hello, Node.js!');
     });

     server.listen(3000, () => {
         console.log('Server is running on http://localhost:3000');
     });
     ```

   - Kör servern med:
     ```bash
     node server.js
     ```


**4. Avslutande tankar och ytterligare resurser**
   - [Node.js dokumentation](https://nodejs.org/en/docs/)

---

**Demonstration 2: Hantera data med Express och Middleware**

**1. Introduktion till Express**
   - Vad är Express?
   - Varför använda Express med Node.js?
   - [Referenslänk](https://expressjs.com/)

**2. Installera Express och skapa en grundläggande app**
   - Installera Express:
     ```bash
     npm install express
     ```

   - Skapa en enkel Express-app i en ny fil `app.js`:
     ```javascript
     const express = require('express');
     const app = express();

     app.get('/', (req, res) => {
         res.send('Hello, Express!');
     });

     app.listen(3000, () => {
         console.log('Express app running on http://localhost:3000');
     });
     ```

   - Kör appen med:
     ```bash
     node app.js
     ```

**3. Introduktion till Middleware och hantera data**
   - Förklara konceptet med middleware i Express.
   - Lägg till middleware för att tolka JSON-data:
     ```javascript
     app.use(express.json());
     ```

   - Skapa en enkel POST-route för att ta emot data:
     ```javascript
     app.post('/data', (req, res) => {
         console.log(req.body);
         res.send('Data received!');
     });
     ```

**4. Avslutande tankar och ytterligare resurser**
   - [Express dokumentation](https://expressjs.com/en/starter/installing.html)
   - [Middleware i Express](https://expressjs.com/en/guide/using-middleware.html)

---

**Demonstration 3: Ansluta till en databas med MongoDB och Mongoose**

**1. Introduktion till MongoDB**
   - Vad är MongoDB?
   - Varför använda en NoSQL-databas?
   - [Referenslänk](https://www.mongodb.com/what-is-mongodb)

**2. Installation av MongoDB och Mongoose**
   - Följ [MongoDB's installationsguide](https://docs.mongodb.com/manual/installation/) för ditt operativsystem.
   - Installera Mongoose (ODM för MongoDB):
     ```bash
     npm install mongoose
     ```

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

**4. Avslutande tankar och ytterligare resurser**
   - [Mongoose dokumentation](https://mongoosejs.com/docs/index.html)
   - [MongoDB University](https://university.mongodb.com/)
