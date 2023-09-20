### Lösningsexempel för Övning 1: Skapa en kortlek

```javascript
let suits = ["Hjärter", "Ruter", "Klöver", "Spader"];
let values = ["2", "3", "4", "5", "6", "7", "8", "9", "10", "Knekt", "Dam", "Kung", "Ess"];
let deck = [];

for (let suit of suits) {
    for (let value of values) {
        deck.push(`${suit} ${value}`);
    }
}
console.log(deck);
```

### Lösningsexempel för Övning 2: Blanda kortleken

```javascript
function shuffleDeck(deck) {
    for (let i = deck.length - 1; i > 0; i--) {
        let j = Math.floor(Math.random() * (i + 1));
        [deck[i], deck[j]] = [deck[j], deck[i]];
    }
    return deck;
}

shuffleDeck(deck);
console.log(deck);
```

### Lösningsexempel för Övning 3: Dela ut kort

```javascript
function dealCards(deck, numCardsPerHand) {
    return deck.splice(0, numCardsPerHand);
}

let player1Hand = dealCards(deck, 5);
let player2Hand = dealCards(deck, 5);
console.log(player1Hand);
console.log(player2Hand);
```

### Lösningsexempel för Övning 4: Hitta ett specifikt kort

```javascript
function containsCard(hand, card) {
    return hand.includes(card);
}

console.log(containsCard(player1Hand, "Hjärter Kung"));
```

### Lösningsexempel för Övning 5: Jämför händer

```javascript
function countAces(hand) {
    return hand.filter(card => card.endsWith("Ess")).length;
}

let player1Aces = countAces(player1Hand);
let player2Aces = countAces(player2Hand);

if (player1Aces > player2Aces) {
    console.log("Spelare 1 har fler ess!");
} else if (player2Aces > player1Aces) {
    console.log("Spelare 2 har fler ess!");
} else {
    console.log("Båda spelarna har samma antal ess!");
}
```
