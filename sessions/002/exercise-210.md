**Git Övningsuppgift för Nybörjare**

**Mål:** Efter att ha slutfört denna övning ska du kunna skapa ett nytt Git-repo, göra ändringar, spåra dem med Git, och återställa tidigare versioner av dina filer.

**Instruktioner:**

1. **Installera Git**
   Om du inte redan har Git installerat, gå till [Git officiella webbsida](https://git-scm.com/) och följ instruktionerna för din operativsystem.

2. **Skapa ett nytt repo**
   - Öppna terminalen eller kommandotolken.
   - Navigera till en katalog där du vill skapa ditt nya Git-repo.
   - Kör följande kommando: `git init my_first_repo`
   - Gå in i katalogen med `cd my_first_repo`

3. **Lägg till en ny fil**
   - Skapa en ny fil med namnet `my_first_file.txt` (du kan använda en textredigerare eller köra kommandot `echo my_first_file.txt`).
   - Öppna filen och skriv något innehåll, till exempel "Detta är min första fil i Git!".

4. **Lägg till filen i Git**
   - Kör kommandot `git add my_first_file.txt`
   - Kontrollera status med `git status`

5. **Commit din första ändring**
   - Kör kommandot `git commit -m "Lade till min första fil"`

6. **Gör fler ändringar**
   - Lägg till mer text i `my_first_file.txt`
   - Kör kommandot `git status` för att se vilka ändringar som har gjorts.
   - Lägg till ändringarna med `git add my_first_file.txt`
   - Gör en ny commit med `git commit -m "Lade till mer innehåll"`

7. **Visa din commit-historik**
   - Kör kommandot `git log` för att se alla dina commits.

8. **Återställ en ändring**
   - Föreställ dig att du inte gillade din senaste ändring och vill återgå till en tidigare version. Identifiera commit-ID för den version du vill återställa från `git log`.
   - Använd `git checkout [commit-ID] -- my_first_file.txt` för att återställa filen till den versionen.

9. **Övriga övningar**
   - Skapa en ny fil, gör ändringar, lägg till den i Git och commit.
   - Ta bort en fil från ditt repo och commit ändringen.
   - Ändra namn på en fil och commit ändringen.

10. **Reflektion**
   - Vad lärde du dig från den här övningen?
   - Vilka steg var svårast?
   - Hur skulle du kunna använda Git i framtida projekt?
