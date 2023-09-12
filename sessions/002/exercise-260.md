**Node.js och Git Tutorial: Förberedelse för en webbserver-applikation**

**Mål:** Förstå grunderna i Node.js, sätt upp en enkel webbserver, och använd Git för versionshantering av din kod.

**1. Introduktion till Node.js**

   - Node.js är en plattform byggd på Chrome's JavaScript runtime som låter dig bygga skalbara nätverksapplikationer.
   - Den används ofta för att bygga backend-system och API:er.

**2. Installera Node.js och Git**

   - Hämta och installera Node.js från [officiell webbplats](https://nodejs.org/).
   - Installera Git från [Git officiella webbsida](https://git-scm.com/).

**3. Sätt upp ditt Node.js-projekt**

   - **Skapa en ny katalog för ditt projekt:**
     ```bash
     mkdir nodejs_webserver
     cd nodejs_webserver
     ```

   - **Initiera ett nytt Node.js-projekt:**
     ```bash
     npm init
     ```
     Följ anvisningarna för att skapa din `package.json`-fil.

   - **Installera Express (ett populärt ramverk för att bygga webbservrar i Node.js):**
     ```bash
     npm install express --save
     ```

**4. Använd Git för versionshantering**

   - **Initiera ett Git-repo i din katalog:**
     ```bash
     git init
     ```

   - **Lägg till en `.gitignore`-fil:**
     Skapa en fil med namnet `.gitignore` och lägg till följande rader:
     ```
     node_modules/
     ```

   - **Commit dina initiala filer:**
     ```bash
     git add .
     git commit -m "Initial commit with Express setup"
     ```

**5. Skapa en grundläggande webbserver med Express**

   - **Skapa en fil `server.js`:**
     
   - Lägg till följande kod:
     ```javascript
     const express = require('express');
     const app = express();
     const PORT = 3000;

     app.get('/', (req, res) => {
         res.send('Hello, Node.js!');
     });

     app.listen(PORT, () => {
         console.log(`Server is running on http://localhost:${PORT}`);
     });
     ```

   - **Kör din server:**
     ```bash
     node server.js
     ```

   - Besök `http://localhost:3000` i din webbläsare. Du bör se meddelandet "Hello, Node.js!".

**6. Versionshantera dina ändringar med Git**

   - **Lägg till och commit dina ändringar:**
     ```bash
     git add .
     git commit -m "Added basic web server functionality"
     ```

**7. Förberedelse inför större övning**

   Nu när du har en grundläggande webbserver och en versionshanterad kodbas med Git, är du redo för mer avancerade övningar. Föreställ dig följande utvecklingssteg:

   - Lägg till fler vägar/endpoints till din server.
   - Använd databaser för att lagra och hämta data.
   - Implementera användarautentisering.
   - Använd externa API:er för att hämta data.
