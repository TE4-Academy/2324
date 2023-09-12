**Introduktion till Postman**

**Mål:** Lär dig grunderna i Postman för att skicka, testa och felsöka API-förfrågningar.

**1. Vad är Postman?**
   
   - Postman är ett populärt verktyg för API-utveckling och testning. Det låter dig skapa, skicka, och analysera förfrågningar till API:er i ett användarvänligt gränssnitt.

**2. Installera Postman**

   - Gå till [Postman's officiella webbsida](https://www.postman.com/downloads/) och ladda ner den senaste versionen för ditt operativsystem.
   - Följ installationsanvisningarna.

**3. Översikt av Postman gränssnittet**

   - **Request-flikar:** Varje ny förfrågan du skapar öppnas i en ny flik, vilket gör det enkelt att växla mellan olika förfrågningar.
   - **HTTP-metoder:** Du kan välja vilken HTTP-metod (GET, POST, PUT, DELETE, etc.) du vill använda för din förfrågan.
   - **Endpoint-URL:** Här skriver du in den URL du vill skicka din förfrågan till.
   - **Parametrar, Headers och Body:** Dessa sektioner låter dig specificera ytterligare detaljer för din förfrågan.
   - **Send-knapp:** Klicka på denna knapp för att skicka din förfrågan.
   - **Respons-sektion:** Här visas svaret från servern när du skickar en förfrågan.

**4. Skicka din första förfrågan**

   - Starta Postman.
   - Skapa en ny förfrågan genom att klicka på "+"-ikonen.
   - Välj "GET" som HTTP-metod.
   - Ange en test-URL, t.ex. `https://api.github.com/users/octocat`.
   - Klicka på "Send".
   - I respons-sektionen bör du se information om GitHub-användaren "octocat".

**5. Arbeta med responsdata**

   - Postman visar responsdata i ett formatat sätt under fliken "Pretty".
   - Du kan även se rådata under fliken "Raw" eller visualisera datan på olika sätt genom att använda "Visualize".

**6. Spara och organisera förfrågningar**

   - Du kan spara en förfrågan genom att klicka på "Save"-knappen.
   - För att organisera dina förfrågningar kan du skapa "Collections". Tänk på dem som mappar där du kan gruppera relaterade förfrågningar.

