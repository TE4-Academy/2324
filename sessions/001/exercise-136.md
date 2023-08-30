## Grundläggande JavaScript baserad på information från Mozilla Developer Network (MDN)

**Del 6: DOM-manipulation**
1. **Teori:** Vad är Document Object Model (DOM) och hur kan JavaScript användas för att förändra det?
   - Hänvisning: [MDN DOM](https://developer.mozilla.org/sv-SE/docs/Web/API/Document_Object_Model/Introduction)
2. **Exempel:** Lägg till och ta bort element från en webbsida dynamiskt.
```html
<button onclick="läggTillElement()">Lägg till</button>
<button onclick="taBortElement()">Ta bort</button>
<ul id="minLista">
    <li>Exempel 1</li>
</ul>

<script>
function läggTillElement() {
    let li = document.createElement("li");
    li.appendChild(document.createTextNode("Nytt element"));
    document.getElementById("minLista").appendChild(li);
}

function taBortElement() {
    let list = document.getElementById("minLista");
    list.removeChild(list.lastChild);
}
</script>
```
3. **Övning:** Skapa en lista på webbsidan där användaren kan lägga till och ta bort listelement via knappar.
