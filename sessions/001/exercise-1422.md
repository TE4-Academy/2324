
**2. Möjlighet att redigera en uppgift:**
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
