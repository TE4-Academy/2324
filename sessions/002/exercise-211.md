**Git Övningsuppgift för Windows-användare**

**Mål:** Efter att ha slutfört denna övning ska du kunna hantera flera versioner av ditt projekt genom att använda grenar, samt sammanfoga dessa grenar.

**Instruktioner:**

1. **Förberedelser**
   - Om du inte redan har Git Bash installerat på din Windows-maskin, ladda ner och installera det från [Git officiella webbsida](https://git-scm.com/).
   - Starta Git Bash.

2. **Skapa ett nytt repo**
   - Följ stegen från förra övningen för att skapa ett.

3. **Skapa en ny gren**
   - Använd kommandot `git branch feature1` för att skapa en ny gren med namnet "feature1".
   - Byt till den nya grenen med `git checkout feature1`.

4. **Gör ändringar på din nya gren**
   - Lägg till en ny fil med namnet `feature1.txt` och skriv något innehåll i den.
   - Kör `git add feature1.txt` och sedan `git commit -m "Lade till feature1.txt"`.

5. **Byt tillbaka till huvudgrenen (master)**
   - Använd kommandot `git checkout master`.

6. **Gör ändringar på huvudgrenen**
   - Lägg till en ny fil med namnet `master_changes.txt` och skriv något innehåll i den.
   - Kör `git add master_changes.txt` och sedan `git commit -m "Lade till master_changes.txt"`.

7. **Sammanfoga grenarna**
   - Nu har du två separata grenar med olika ändringar. Ditt mål är att sammanfoga dessa ändringar i huvudgrenen.
   - Medan du är på master-grenen, kör `git merge feature1`.
   - Om det inte finns några konflikter, har du framgångsrikt sammanfogat grenarna!

8. **Hantera sammanfogningskonflikter (om de uppstår)**
   - Om det uppstår en konflikt under sammanslagningen, kommer Git att meddela dig.
   - Öppna den berörda filen i en textredigerare. Git kommer att markera de konflikterande delarna.
   - Manuellt redigera filen för att lösa konflikten och ta bort Git-markeringarna.
   - När du har löst konflikten, kör `git add [filnamn]` och sedan `git commit`.

9. **Reflektion**
   - Hur kändes det att arbeta med grenar?
   - Hur skulle grenar kunna vara användbara i större projekt?
   - Vad lärde du dig om att hantera konflikter?

