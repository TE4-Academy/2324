### Övning 1: Skapa och visa en array

**Uppgift:** Skapa en array med namnen på veckodagarna och visa dem i konsolen.

**Lösningsexempel:**
```javascript
let days = ["Måndag", "Tisdag", "Onsdag", "Torsdag", "Fredag", "Lördag", "Söndag"];
console.log(days);
```

### Övning 2: Lägga till och ta bort element

**Uppgift:** Skapa en array med tre fruktnamn. Lägg till en frukt i slutet av arrayen och ta sedan bort den första frukten från arrayen.

**Lösningsexempel:**
```javascript
let fruits = ["Äpple", "Banan", "Citron"];
fruits.push("Druva");
fruits.shift();
console.log(fruits);  // Förväntat resultat: ["Banan", "Citron", "Druva"]
```

### Övning 3: Accessa ett specifikt element

**Uppgift:** Skapa en array med namnen på månaderna. Visa namnet på den sjätte månaden i konsolen.

**Lösningsexempel:**
```javascript
let months = ["Januari", "Februari", "Mars", "April", "Maj", "Juni", "Juli", "Augusti", "September", "Oktober", "November", "December"];
console.log(months[5]);  // Förväntat resultat: "Juni"
```

### Övning 4: Loopa genom en array

**Uppgift:** Skapa en array med siffrorna från 1 till 5. Använd en `for`-loop för att visa varje siffra i konsolen.

**Lösningsexempel:**
```javascript
let numbers = [1, 2, 3, 4, 5];
for (let i = 0; i < numbers.length; i++) {
    console.log(numbers[i]);
}
```

### Övning 5: Hitta ett element i en array

**Uppgift:** Skapa en array med några färger. Använd metoden `includes` för att kontrollera om "Blå" finns i din array och visa resultatet i konsolen.

**Lösningsexempel:**
```javascript
let colors = ["Röd", "Grön", "Blå", "Gul"];
let containsBlue = colors.includes("Blå");
console.log(containsBlue);  // Förväntat resultat: true
```

Genom att arbeta igenom dessa övningar bör du få en bättre förståelse för hur arrays fungerar i JavaScript, hur du kan manipulera dem och hur du kan interagera med dem.
