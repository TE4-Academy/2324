**Postman Tutorial: Testa CRUD-operationer för ditt Node.js API**

**Mål:** Förstå hur man använder Postman för att testa CRUD-operationer på ditt Node.js API.

**1. Introduktion till Postman**
   
   - Postman är ett populärt verktyg för att utveckla och testa API:er. Med Postman kan du skicka förfrågningar till ditt API och se svaren i ett användarvänligt gränssnitt.

**2. Installera Postman**

   - Gå till [Postman's officiella webbsida](https://www.postman.com/downloads/) och ladda ner den senaste versionen för ditt operativsystem.
   - Följ installationsanvisningarna.

**3. Starta Postman och skapa en ny Collection**

   - När Postman är installerat, starta programmet.
   - Skapa en ny Collection genom att klicka på "New" och välja "Collection". Döp den till "Node.js CRUD".

**4. Testa CRUD-operationer med Postman**

   - Se till att din Node.js-server (från den tidigare övningen) körs.

   - **Läs (Read) alla böcker:**
     - Klicka på "+" för att skapa en ny flik.
     - Välj "GET" och ange din endpoint-URL: `http://localhost:3000/books`.
     - Klicka på "Send". Du bör se en lista över böcker i svaret.

   - **Lägg till (Create) en ny bok:**
     - Skapa en ny flik.
     - Välj "POST" och ange din endpoint-URL: `http://localhost:3000/books`.
     - Gå till "Body", välj "raw" och "JSON (application/json)".
     - Skriv in din bokdata i JSON-format, t.ex.:
       ```json
       {
           "title": "A New Book",
           "author": "Some Author"
       }
       ```
     - Klicka på "Send". Du bör se den nyskapade boken i svaret.

   - **Uppdatera (Update) en befintlig bok:**
     - Skapa en ny flik.
     - Välj "PUT" och ange din endpoint-URL med bokens ID: `http://localhost:3000/books/1`.
     - Följ samma steg som ovan för att lägga till body-data och uppdatera bokinformationen.
     - Klicka på "Send". Du bör se den uppdaterade boken i svaret.

   - **Ta bort (Delete) en bok:**
     - Skapa en ny flik.
     - Välj "DELETE" och ange din endpoint-URL med bokens ID: `http://localhost:3000/books/1`.
     - Klicka på "Send". Du bör se den borttagna boken i svaret.

**5. Spara dina förfrågningar**

   - För varje flik du har öppnat, klicka på "Save" och spara förfrågan i din "Node.js CRUD" Collection. Detta gör att du snabbt kan återanvända och testa dessa förfrågningar i framtiden.
