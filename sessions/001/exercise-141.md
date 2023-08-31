# Övning: En enkel interaktiv uppgiftshanterare

## Beskrivning: 
### Skapa en enkel webbapplikation där användaren kan lägga till uppgifter, markera dem som klara och ta bort dem. Denna övning kommer att kombinera många av de koncept du har lärt dig, inklusive DOM-manipulation, händelsehantering och grundläggande JavaScript-logik

**Steg 1:** Skapa HTML-strukturen.
```html
<!DOCTYPE html>
<html lang="sv">
<head>
    <title>Uppgiftshanterare</title>
</head>
<body>
    <h2>Min Uppgiftshanterare</h2>
    <input type="text" id="nyUppgift" placeholder="Lägg till ny uppgift">
    <button onclick="läggTillUppgift()">Lägg till</button>
    <ul id="uppgiftsLista"></ul>
    <script src="script.js"></script>
</body>
</html>
```

**Steg 2:** Skapa `script.js` för din JavaScript-kod.

**Funktion för att lägga till en uppgift:**
```javascript
function läggTillUppgift() {
    let uppgiftsText = document.getElementById('nyUppgift').value;

    if (uppgiftsText === "") {
        alert("Vänligen skriv en uppgift!");
        return;
    }

    let li = document.createElement("li");
    li.innerHTML = uppgiftsText + ' <button onclick="taBortUppgift(this)">Ta bort</button> <button onclick="markeraKlar(this)">Klar</button>';

    document.getElementById('uppgiftsLista').appendChild(li);
    document.getElementById('nyUppgift').value = '';
}
```

**Funktion för att ta bort en uppgift:**
```javascript
function taBortUppgift(button) {
    let li = button.parentElement;
    li.parentElement.removeChild(li);
}
```

**Funktion för att markera en uppgift som klar:**
```javascript
function markeraKlar(button) {
    let li = button.parentElement;
    li.style.textDecoration = "line-through";
    button.disabled = true;
}
```

När detta är klart borde du ha en fungerande uppgiftshanterare där du kan lägga till uppgifter, markera dem som klara och ta bort dem.
