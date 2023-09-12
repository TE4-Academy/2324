# FizzBuzz! 
Ett populärt programmeringsproblem som används för att testa en kandidats förståelse för grunderna i programmering. 
Här är en steg-för-steg tutorial som förbereder dig att skriva ett FizzBuzz-program i JavaScript:

**JavaScript FizzBuzz Tutorial**

**Mål:** Förstå grunderna i JavaScript för att kunna skriva ett FizzBuzz-program.
**OBS:** Du måste använda Git genom hela processen, och beskriva de olika momenten per commit. 
När du är helt klar, skapa ett "bare" (tomt) GitHub repo och koppla ihop dem och pusha upp.

**1. Introduktion till JavaScript**
   - JavaScript är ett högnivåspråk som oftast används för webbprogrammering.
   - Det kan köras i alla moderna webbläsare utan behov av kompilerare eller särskilda verktyg.

**2. Grundläggande syntax**

   - **Variabler:** Används för att lagra data.
     ```javascript
     var number = 5;
     ```

   - **Funktioner:** Återanvändbara kodblock.
     ```javascript
     function sayHello() {
       console.log("Hello!");
     }
     ```

   - **Villkor:** Används för att testa ett villkor och köra olika kodblock beroende på utfallet.
     ```javascript
     if (number === 5) {
       console.log("Number is 5");
     } else {
       console.log("Number is not 5");
     }
     ```

   - **Loopar:** Kör kod flera gånger.
     ```javascript
     for (var i = 0; i < 10; i++) {
       console.log(i);
     }
     ```

**3. FizzBuzz-Regler**
   - Skriv ut nummer från 1 till 100.
   - För varje nummer som är en multipel av 3, skriv ut "Fizz".
   - För varje nummer som är en multipel av 5, skriv ut "Buzz".
   - För nummer som är en multipel av både 3 och 5, skriv ut "FizzBuzz".
   - För alla andra nummer, skriv ut numret.

**4. Steg för att skriva FizzBuzz**

   1. Skapa en loop som går från 1 till 100.
   2. Inuti loopen, testa villkoren för Fizz, Buzz och FizzBuzz med hjälp av if-satser.
   3. Använd `console.log()` för att skriva ut resultaten.

**5. Exempelkod för FizzBuzz**

```javascript
for (var i = 1; i <= 100; i++) {
  if (i % 3 === 0 && i % 5 === 0) {
    console.log("FizzBuzz");
  } else if (i % 3 === 0) {
    console.log("Fizz");
  } else if (i % 5 === 0) {
    console.log("Buzz");
  } else {
    console.log(i);
  }
}
```

**6. Testa din kod**
   - Öppna din webbläsares konsol (t.ex. i Chrome, högerklicka någonstans på sidan, välj "Inspektera" och gå till "Console"-fliken).
   - Klistra in din FizzBuzz-kod och tryck Enter. Du bör se utskrifterna från 1 till 100, med "Fizz", "Buzz" och "FizzBuzz" på lämpliga platser.

**7. Övningar**

   1. Anpassa programmet för att gå från 1 till 200.
   2. Lägg till ytterligare ett villkor: för nummer som är en multipel av 7, skriv ut "Boom".
   3. Ändra programmet så att det tar två parametrar: `start` och `end`, så att du kan bestämma vilka nummer att börja och sluta loopen med.

