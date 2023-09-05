**Git Övningsuppgift: Lokalt till Remote**

**Mål:** Efter att ha slutfört denna övning ska du kunna hantera ditt projekt både lokalt och på en fjärrserver (GitHub i detta fall), förstå och hantera sammanslagningskonflikter, och effektivt spåra ditt arbete med `git log`.


**Instruktioner:**

1. **Förberedelser**
   - Om du inte redan har ett GitHub-konto, skapa ett på [GitHub.com](https://github.com/).
   - Installera Git (om inte redan gjort) och konfigurera din användarinformation.

2. **Skapa ett nytt lokalt repo**
   - Använd `git init project_repo` för att skapa ett nytt lokalt repo.

3. **Arbeta med grenar**
   - Skapa en ny gren med `git branch development`.
   - Byt till den nya grenen med `git checkout development`.
   - Lägg till en fil, t.ex. `dev_file.txt`, commita den.

4. **Skapa ett fjärr-bare-repo på GitHub**
   - Logga in på GitHub och skapa ett nytt repo med namnet "project_repo" (utan att initialisera det med en README).

5. **Koppla ditt lokala repo till det fjärrstyrda repot och pusha**
   - Använd `git remote add origin [URL till ditt GitHub-repo]`.
   - Pusha din development-gren till GitHub med `git push -u origin development`.

6. **Skillnaden mellan `fetch` och `pull`**
   - Gör en ändring direkt på GitHub i `dev_file.txt` (t.ex. via webbgränssnittet).
   - Lokalt, kör `git fetch`. Observera att dina lokala filer inte ändras.
   - Kör `git pull` och märk hur dina lokala filer nu uppdateras med ändringarna från GitHub.

7. **Hantera sammanslagningskonflikter**
   - Lokalt, gör en ändring i `dev_file.txt` utan att pusha den till GitHub.
   - På GitHub, gör en annan ändring i samma del av `dev_file.txt`.
   - Försök nu att `pull` från ditt lokala repo. En konflikt kommer att uppstå.
   - Lös konflikten manuellt, lägg till filen och commita den.

8. **Utforska `git log`**
   - Kör `git log` för att se en lista över commits.
   - Prova några olika flaggor som `--oneline`, `--graph`, `--all`, `--decorate` för att se olika presentationer av loggen.

9. **Skapa en bug och hantera den med en gren och sammanslagning**
   - Introducera en "bug" i din kod (t.ex. en felaktig rad i `dev_file.txt`).
   - Skapa en ny gren med `git branch bugfix`.
   - Byt till den nya grenen, fixa buggen och commita dina ändringar.
   - Byt tillbaka till `development`-grenen och slå samman `bugfix`-grenen med `git merge bugfix`.


