### Övning 6: Array-metoden `map()`
**Uppgift:** Skapa en array med siffrorna 1 till 5. Använd `map()` för att skapa en ny array där varje siffra multipliceras med 10.

**Lösningsexempel:**
```javascript
let numbers = [1, 2, 3, 4, 5];
let multiplied = numbers.map(num => num * 10);
console.log(multiplied);  // Förväntat resultat: [10, 20, 30, 40, 50]
```

### Övning 7: Array-metoden `filter()`
**Uppgift:** Skapa en array med siffrorna 1 till 10. Använd `filter()` för att skapa en ny array som endast innehåller jämna siffror.

**Lösningsexempel:**
```javascript
let numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let evens = numbers.filter(num => num % 2 === 0);
console.log(evens);  // Förväntat resultat: [2, 4, 6, 8, 10]
```

### Övning 8: Array-metoden `reduce()`
**Uppgift:** Skapa en array med siffrorna 1 till 5. Använd `reduce()` för att beräkna summan av alla siffror i arrayen.

**Lösningsexempel:**
```javascript
let numbers = [1, 2, 3, 4, 5];
let sum = numbers.reduce((acc, num) => acc + num, 0);
console.log(sum);  // Förväntat resultat: 15
```

### Övning 9: Array-metoden `find()`
**Uppgift:** Skapa en array med objekt där varje objekt representerar en bok med en titel och en författare. Använd `find()` för att hitta boken med titeln du specificerar.

**Lösningsexempel:**
```javascript
let books = [
  {title: "Boken A", author: "Författare A"},
  {title: "Boken B", author: "Författare B"},
  {title: "Boken C", author: "Författare C"}
];

let book = books.find(b => b.title === "Boken B");
console.log(book);  // Förväntat resultat: {title: "Boken B", author: "Författare B"}
```

### Övning 10: Kombinera flera array-metoder
**Uppgift:** Skapa en array med siffrorna 1 till 10. Använd en kombination av `map()`, `filter()`, och `reduce()` för att först filtrera ut jämna siffror, sedan multiplicera varje siffra med 10, och slutligen summera alla siffror i den resulterande arrayen.

**Lösningsexempel:**
```javascript
let numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let result = numbers
  .filter(num => num % 2 === 0)
  .map(num => num * 10)
  .reduce((acc, num) => acc + num, 0);
console.log(result);  // Förväntat resultat: 300 (2*10 + 4*10 + 6*10 + 8*10 + 10*10)
```

Genom att utforska dessa övningar kommer du att få en djupare förståelse för hur arrayer fungerar i JavaScript, särskilt de inbyggda metoderna som kan användas för att bearbeta och interagera med array-data.
