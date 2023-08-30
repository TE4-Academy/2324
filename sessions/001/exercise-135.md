## Grundläggande JavaScript baserad på information från Mozilla Developer Network (MDN)

**Del 5: Händelsehantering**
1. **Teori:** Hur interagerar JavaScript med webbsidans element genom händelsehantering?
   - Hänvisning: [MDN Händelsehantering](https://developer.mozilla.org/sv-SE/docs/Learn/JavaScript/Building_blocks/Events)
2. **Exempel:** Ändra texten i en paragraf när en knapp klickas på.
```html
<button onclick="ändraText()">Klicka här!</button>
<p id="demo">Detta kommer att ändras.</p>

<script>
function ändraText() {
    document.getElementById("demo").innerHTML = "Texten har ändrats!";
}
</script>
```
3. **Övning:** Skapa en knapp som byter färg på en div när den klickas på.

