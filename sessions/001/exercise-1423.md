**3. Spara uppgifterna i webbläsarens `localStorage`:**
För att göra detta behöver du uppdatera när du lägger till, tar bort och markerar uppgifter för att spara listan till `localStorage`. Dessutom behöver du läsa in uppgifterna när sidan laddas.

Lägg till följande kod i `läggTillUppgift`-funktionen, efter att du har lagt till en uppgift:
```javascript
let uppgifter = JSON.parse(localStorage.getItem("uppgifter") || "[]");
uppgifter.push(uppgiftsText);
localStorage.setItem("uppgifter", JSON.stringify(uppgifter));
```

Lägg till detta i `taBortUppgift`-funktionen, efter att du har tagit bort en uppgift:
```javascript
let uppgifter = JSON.parse(localStorage.getItem("uppgifter"));
let uppgiftIndex = uppgifter.indexOf(li.textContent.slice(0, -12)); // -12 to remove the 'Ta bort Klar' text
uppgifter.splice(uppgiftIndex, 1);
localStorage.setItem("uppgifter", JSON.stringify(uppgifter));
```

Lägg till en funktion för att ladda uppgifter när sidan laddas:
```javascript
window.onload = function() {
    let uppgifter = JSON.parse(localStorage.getItem("uppgifter") || "[]");
    for (let uppgift of uppgifter) {
        let li = document.createElement("li");
        li.innerHTML = uppgift + ' <button onclick="taBortUppgift(this)">Ta bort</button> <button onclick="markeraKlar(this)">Klar</button>';
        document.getElementById('uppgiftsLista').appendChild(li);
    }
}
```
