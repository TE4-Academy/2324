## Fördjupad Nätverksanalys med Chrome DevTools

**Mål:** Efter denna utökade övning bör du ha en djupare förståelse för hur du kan analysera nätverksförfrågningar och prestanda med hjälp av DevTools.

**Förutsättningar:** Samma som tidigare; du har Google Chrome och kan öppna DevTools.

---

**3. Nätverksanalys (Utökad)**

**a. Grundläggande översikt**

- Välj "Network"-fliken i DevTools.
- Uppdatera webbsidan.
- Observera de olika typerna av förfrågningar (t.ex. Stylesheet, Script, Image, XHR).
- Notera responstiderna, statuskoderna (t.ex. 200, 404, 301) och filstorlekarna.

**b. Filtrera förfrågningar**

- Använd filterfältet ovanför förfrågningslistan för att filtrera specifika typer av förfrågningar, t.ex. "JS" för bara JavaScript-filer.
- Du kan också filtrera för att hitta filer med specifika statuskoder, t.ex. `status-code:404` för att hitta "not found" förfrågningar.

**c. Undersök en enskild förfrågan**

- Klicka på en av förfrågningarna för att öppna detaljpanelen.
- Under "Headers" kan du se detaljerad information om förfrågan, inklusive request och response headers.
- "Preview" visar en förhandsvisning av förfrågan, vilket kan vara särskilt användbart för bilder eller JSON-respons.
- "Response" visar det exakta innehållet som returneras från servern.
- "Timing" ger en detaljerad tidsuppdelning av förfrågningen.

**d. Simulera olika nätverksförhållanden**

- I "Network"-fliken, leta efter rullgardinsmenyn bredvid det röda inspelningsknappen uppe till vänster. Standardinställningen är "No throttling."
- Välj olika förhållanden, t.ex. "Fast 3G" eller "Slow 3G", för att simulera hur webbplatsen laddar under dessa förhållanden.
- Uppdatera webbsidan och observera hur belastningstiderna påverkas. Detta är särskilt användbart för att förstå upplevelsen för användare med långsammare internetanslutningar.

**e. Blockera specifika förfrågningar**

- Högerklicka på en förfrågan i listan och välj "Block request URL".
- Uppdatera webbsidan. Observera hur sidan laddar (eller inte laddar) utan den blockerade resursen. Detta kan vara användbart för att identifiera flaskhalsar eller problem med specifika resurser.

---

Genom att bemästra dessa färdigheter kan du effektivt identifiera problem, optimera lasttider och förbättra webbplatsens prestanda. Nätverksanalys är ett kraftfullt verktyg i en utvecklares verktygslåda, och att kunna använda det effektivt kan leda till avsevärda förbättringar i användarupplevelsen.
