# Övningar att göra i [Mozilla Play](https://developer.mozilla.org/en-US/play)
För referens, titta gärna på länkarna i [Exercise 151](https://github.com/TE4-Academy/2324/blob/main/sessions/001/exercise-151.md)
1. **Variabler**
   - Exempel:
     ```javascript
     let dag = "Måndag";
     const maxPersoner = 50;
     var färg = "Blå";
     ```

   - **Uppgift:** Skapa en variabel `hobby` och tilldela den en sträng som beskriver din favorithobby. Logga sedan variabeln i konsolen.

2. **Funktioner**
   - Exempel:
     ```javascript
     function kvadrat(x) {
         return x * x;
     }
     ```

   - **Uppgift:** Skapa en funktion som heter `hälsning` som tar ett namn som argument och returnerar en sträng som säger "Hej [namn]!". Anropa funktionen med ditt namn.

3. **Objekt och egenskaper**
   - Exempel:
     ```javascript
     let bil = {
         märke: "Volvo",
         modell: "XC60",
         årsmodell: 2020
     };
     console.log(bil.märke); // "Volvo"
     ```

   - **Uppgift:** Skapa ett objekt `film` med egenskaperna `titel`, `regissör` och `år`. Fyll i med information om din favoritfilm och logga filmens titel i konsolen.

4. **Kontrollstrukturer**
   - Exempel:
     ```javascript
     let temperatur = 15;
     if (temperatur < 20) {
         console.log("Det är lite kyligt.");
     } else {
         console.log("Det är varmt!");
     }
     ```

   - **Uppgift:** Skapa en variabel `antalÄpplen` och tilldela den ett värde mellan 0 och 10. Använd en `if`-sats för att skriva ut ett meddelande baserat på om det finns några äpplen eller inte.

5. **Händelsehantering**
   - Exempel:
     ```html
     <button id="minKnapp">Klicka mig</button>
     <script>
         document.getElementById('minKnapp').addEventListener('click', function() {
             alert('Tack för att du klickade!');
         });
     </script>
     ```

   - **Uppgift:** Lägg till en knapp i din HTML. Skriv JavaScript-kod som visar en alert med texten "Knappen klickades!" när användaren klickar på knappen.

6. **Arrayer och Loopar**
   - Exempel:
     ```javascript
     let djur = ["katt", "hund", "fisk"];
     for (let i = 0; i < djur.length; i++) {
         console.log(djur[i]);
     }
     ```

   - **Uppgift:** Skapa en array med namnen på tre av dina vänner. Använd en `for`-loop för att skriva ut varje namn på en ny rad i konsolen.

För varje uppgift kan du använda en webbläsares konsol eller en online-utvecklingsmiljö som JSFiddle eller CodePen för att skriva och testa din kod.
