# I övningen användes flera olika språkdelar i JavaScript. 
## Låt oss gå igenom dem:

1. **Variabler**
   - Används för att lagra och referera till data.
   - Exempel från övningen:
     ```javascript
     let uppgiftsText = document.getElementById('nyUppgift').value;
     let kategori = document.getElementById('kategori').value;
     let prioritet = document.getElementById('prioritet').value;
     ```
   - **MDN:** [Var](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var), [Let](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let), [Const](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const)
   - **W3 Schools:** [JavaScript Variables](https://www.w3schools.com/js/js_variables.asp)


2. **Funktioner**
   - Block av kod som kan anropas flera gånger.
   - Exempel från övningen:
     ```javascript
     function läggTillUppgift() { ... }
     function sorteraUppgifter(kriterium) { ... }
     ```
   - **MDN:** [Function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions)
   - **W3 Schools:** [JavaScript Functions](https://www.w3schools.com/js/js_functions.asp)

3. **Objekt och egenskaper**
   - Används för att interagera med HTML-element och deras attribut.
   - Exempel från övningen:
     ```javascript
     document.getElementById('nyUppgift').value;
     li.innerHTML;
     ```
   - **MDN:** [Objects Basics](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics)
   - **W3 Schools:** [JavaScript Objects](https://www.w3schools.com/js/js_objects.asp)
     
4. **Kontrollstrukturer**
   - Används för att utföra olika åtgärder beroende på ett villkor.
   - Exempel från övningen:
     ```javascript
     if (uppgiftsText === "") { ... }
     while (lista.firstChild) { ... }
     ```
   - **MDN:** [Control flow and error handling](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling)
   - **W3 Schools:** [JavaScript If...Else](https://www.w3schools.com/js/js_if_else.asp)
     
5. **Händelsehantering**
   - Lyssnar efter specifika händelser, som ett knapptryck.
   - Exempel från övningen:
     ```html
     <button onclick="läggTillUppgift()">Lägg till</button>
     ```
   - **MDN:** [Introduction to events](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events)
   - **W3 Schools:** [HTML DOM Events](https://www.w3schools.com/js/js_htmldom_events.asp)

6. **Arrayer och Loopar**
   - För att manipulera listor av element.
   - Exempel från övningen:
     ```javascript
     let uppgifter = Array.from(lista.getElementsByTagName('li'));
     for (let uppgift of uppgifter) { ... }
     ```
   - **MDN:** [Arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array), [Loops and iteration](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration)
   - **W3 Schools:** [JavaScript Arrays](https://www.w3schools.com/js/js_arrays.asp), [JavaScript Loops](https://www.w3schools.com/js/js_loop_for.asp)

### Dessa är de primära språkdelarna som användes i övningen. 
Varje del spelar en viktig roll i att skapa den dynamiska funktionaliteten i "Att göra"-listan.

