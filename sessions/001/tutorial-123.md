## Practice the basics of C#, including variables, loops, and the Console class.

**Task: Number Guessing Game**

Create a console application that generates a random number between 1 and 100 and allows the user to guess the number. The program should give hints to the user if the guessed number is too high or too low. If the user guesses the number correctly, the program should congratulate the user and show the number of attempts it took to guess the number correctly.

**Steps:**

1. **Setup the project:** Create a new C# console application. You can do this in Visual Studio by going to `File -> New -> Project`, then select `Console App (.NET Core)`.

2. **Generate a random number:** Use the `Random` class in C# to generate a random number between 1 and 100. Store this number in a variable.

```csharp
Random random = new Random();
int randomNumber = random.Next(1, 101);
```

3. **Create a loop for user input:** Use a `while` loop to continuously ask the user for their guess. Use the `Console.ReadLine()` method to get the user's input and convert it to an integer using `int.Parse()` or `int.TryParse()`.

```csharp
int userGuess = 0;
while (userGuess != randomNumber)
{
    Console.Write("Enter your guess: ");
    userGuess = int.Parse(Console.ReadLine());
}
```

4. **Give hints to the user:** Inside the loop, add `if` statements to check if the user's guess is too high, too low, or correct. Use the `Console.WriteLine()` method to give feedback to the user.

```csharp
if (userGuess > randomNumber)
{
    Console.WriteLine("Too high! Try again.");
}
else if (userGuess < randomNumber)
{
    Console.WriteLine("Too low! Try again.");
}
else
{
    Console.WriteLine("Congratulations! You guessed the number correctly.");
}
```

5. **Count the attempts:** Add a counter variable to keep track of how many guesses the user has made. Increment the counter each time the user makes a guess.

```csharp
int attempts = 0;
// Inside the loop
attempts++;
```

6. **Display the number of attempts:** When the user guesses the number correctly, display the number of attempts it took them.

```csharp
Console.WriteLine($"It took you {attempts} attempts to guess the number correctly.");
```

Remember to test your program thoroughly to make sure it works as expected. Happy coding!
