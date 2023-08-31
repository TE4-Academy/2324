**1. Lägg till ett filter:**
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
