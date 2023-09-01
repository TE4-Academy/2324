## Praktisk övning: Grundläggande funktioner i Chrome Developer Tools (DevTools)

**Mål:** Efter denna övning bör du ha en grundläggande förståelse för hur man använder några av de centrala funktionerna i Chrome DevTools.

**Förutsättningar:** Du har Google Chrome installerat och kan öppna DevTools (vanligtvis via `Ctrl + Shift + I` på Windows/Linux eller `Cmd + Option + I` på Mac).

---

**1. Inspektera element**

- Öppna valfri webbsida i Chrome. (Exempelvis huddinge.se)
- Högerklicka på ett element (t.ex. en knapp eller text) och välj "Inspect" (eller "Inspektera").
- Notera hur elementet markeras i "Elements"-panelen i DevTools. Här kan du se och redigera HTML och CSS i realtid.

**2. Konsollogga**

- Välj "Console"-fliken i DevTools.
- Skriv `console.log("Hello, DevTools!");` och tryck Enter.
- Observera att meddelandet visas. Konsolen används ofta för att logga fel, varningar eller annan information under kodens utförande.

**3. Nätverksanalys**

- Välj "Network"-fliken i DevTools.
- Uppdatera webbsidan (F5 eller Ctrl+R).
- Observera alla nätverksförfrågningar som görs när sidan laddas. Här kan du se detaljer som responstid, filstorlek och mer.

**4. Debuggera JavaScript**

- Öppna en webbsida med interaktiva element (t.ex. en knapp som utlöser en funktion).
- Välj "Sources"-fliken i DevTools.
- Hitta JavaScript-koden för det interaktiva elementet och placera en brytpunkt genom att klicka på radnumret.
- Interagera med elementet på webbsidan. Exekveringen bör pausa på din brytpunkt, låt dig stega genom koden.

**5. Ändra enhetsvy**

- Klicka på ikonen "Toggle device toolbar" (eller "Växla enhetsverktygsfältet") nära övre vänstra hörnet av DevTools.
- Välj olika enheter eller skärmstorlekar för att se hur webbsidan ser ut på olika enheter. Detta är användbart för responsiv webbdesign.

---

