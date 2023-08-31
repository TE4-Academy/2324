**1. Spara uppgifterna i webbläsarens `localStorage`:**
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

**2. Lägg till ett filter:**
Lägg till dessa radioknappar i din HTML:
```html
<label><input type="radio" name="filter" value="alla" checked onclick="filtreraUppgifter()"> Alla</label>
<label><input type="radio" name="filter" value="klara" onclick="filtreraUppgifter()"> Klara</label>
<label><input type="radio" name="filter" value="ofärdiga" onclick="filtreraUppgifter()"> Ofärdiga</label>
```

Lägg till `filtreraUppgifter`-funktionen:
```javascript
function filtreraUppgifter() {
    let val = document.querySelector('input[name="filter"]:checked').value;
    let liElements = document.getElementById('uppgiftsLista').getElementsByTagName('li');

    for (let li of liElements) {
        switch (val) {
            case "alla":
                li.style.display = '';
                break;
            case "klara":
                li.style.textDecoration === "line-through" ? li.style.display = '' : li.style.display = 'none';
                break;
            case "ofärdiga":
                li.style.textDecoration !== "line-through" ? li.style.display = '' : li.style.display = 'none';
                break;
        }
    }
}
```

**3. Möjlighet att redigera en uppgift:**
Lägg till `redigeraUppgift`-funktionen och använd den i din HTML:
```javascript
function redigeraUppgift(liElement) {
    let nyText = prompt("Redigera uppgift:", liElement.textContent.slice(0, -12));
    if (nyText !== null && nyText !== "") {
        liElement.childNodes[0].nodeValue = nyText;
        
        // Uppdatera localStorage om du använder den funktionen
        let uppgifter = JSON.parse(localStorage.getItem("uppgifter"));
        let uppgiftIndex = uppgifter.indexOf(liElement.textContent.slice(0, -12));
        uppgifter[uppgiftIndex] = nyText;
        localStorage.setItem("uppgifter", JSON.stringify(uppgifter));
    }
}
```

Uppdatera din `<li>` skapelse i `läggTillUppgift` och `window.onload` funktionerna:
```javascript
li.innerHTML = uppgift + ' <button onclick="taBortUppgift(this)">Ta bort</button> <button onclick="markeraKlar(this)">Klar</button>';
li.onclick = function(event) {
    // Kontrollera att klicket inte var på en knapp
    if (event.target.tagName !== "BUTTON") {
        redigeraUppgift(this);
    }
};
```
