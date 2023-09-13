**Större Övningsuppgift: Skapa en webbaserad bokhandel med Node.js**

**Mål:** Bygg en fullständig webbserver med CRUD-operationer för att hantera en bokhandels inventering. Användaren ska kunna lägga till, redigera, visa och ta bort böcker.

**1. Förberedelser**

- Kontrollera att du har Node.js och MongoDB installerade.
- Skapa en ny mapp för ditt projekt:
  ```bash
  mkdir online_bookstore
  cd online_bookstore
  npm init -y
  ```
- Installera nödvändiga paket:
  ```bash
  npm install express mongoose
  ```

**2. Skapa servern med Express**

- Använd kunskapen från tidigare demonstrationer för att sätta upp en grundläggande Express-server.
- Skapa routes för:
  - Hem (t.ex. `/`)
  - Visa alla böcker (t.ex. `/books`)
  - Visa en specifik bok (t.ex. `/books/:id`)

**3. Anslut till MongoDB och skapa databasmodeller med Mongoose**

- Anslut till MongoDB genom att konfigurera en uppkoppling med Mongoose.
- Skapa en Mongoose-modell för böcker med attributen: `title`, `author`, `publishedDate`, `price`, och `description`.

**4. Implementera CRUD-operationer**

- **Lägg till en ny bok:**
  Skapa en POST-route där användaren kan skicka data för att lägga till en ny bok i databasen.
  
- **Visa alla böcker:**
  Skapa en GET-route för att hämta och visa alla böcker i databasen.
  
- **Redigera en befintlig bok:**
  Använd en PUT-route för att uppdatera information om en befintlig bok baserat på bokens ID.
  
- **Ta bort en bok:**
  Använd en DELETE-route för att ta bort en bok baserat på bokens ID.

**5. Testa din applikation med Postman**

- Använd Postman för att skicka förfrågningar till din server och verifiera att alla CRUD-operationer fungerar korrekt.

**6. Felsökning och optimering**

- Gå igenom din kod och kontrollera eventuella fel eller buggar.
- Tänk på eventuella förbättringar eller optimeringar du kan göra i din kod.

