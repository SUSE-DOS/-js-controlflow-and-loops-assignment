[<img src="assets/images/su-logo.png" alt="Skills Union Logo" height="80px" />](https://www.skillsunion.com/)

# JavaScript Control-Flow & Loops: Assignment

## Problems

### 1: Nightclub Bouncer

Using an `if/else` expression, write code that prompts the user for their age, then:

- If the user is older than 18, he/she should receive a message that he/she may enter.
- If the user is younger than 18, then he/she can't enter and should receive a message telling him/her that he/she's too young.
- If the user is between 18 and 21, he/she should receive a message that he/she can enter, but not drink.
- If the user is older than 21, he/she should receive a message that he/she can both enter and drink.

```js
let age = parseInt(
  prompt("'Ello mate, what's your age? Got to be 18 to come in 'ere!", 0)
);

if (age >= 21) {
  console.log("You can enter and have a drink, enjoy!");
} else if (age >= 18 && age < 21) {
  console.log("You can enter, but no drink for you!");
  console.log("go on, enter.");
} else {
  console.log("Too young, YOU SHALL NOT PASS!!");
}
```

### 2: Fizzbuzz

This might feel like a abstract problem. But trust us, it frequently comes up during technical interviews when you are applying for a role as a Software Engineer. So you might as well get a head start on it with a basic version of Fizzbuzz.

In case you are wondering what is [Fizzbuzz](https://en.wikipedia.org/wiki/Fizz_buzz) about. Also, you're going to need the [remainder/modulus operator​](https://javascript.info/operators#remainder) for this.

For version 1 of this problem, only use `if/elseif/else` expressions to solve it.

- Write a program that declares a variable with a random value between 0 and 100 picked by you
- If it is a multiple of 3, print “Fizz” instead of the number
- If it is a multiple of 5, print “Buzz” instead of the number
- If it is a multiple of both 3 and 5, print “FizzBuzz” instead of the number
- Otherwise, print the number

```js
for (let i = 1; i <= 100; i++) {
  if (i % 15 === 0) {
    console.log("FizzBuzz");
  } else if (i % 5 === 0) {
    console.log("Buzz");
  } else if (i % 3 === 0) {
    console.log("Fizz");
  } else {
    console.log(i);
  }
}
```

### 3: The Grade Assigner

- Using a `for` loop check each value from `60` to `100`
- For every value, your `console.log` should show "For 89, you got a B. For 90, you got an A.", etc.

**Legend:**

- A: `90-100`
- B: `80-89`
- C: `70-79`
- D: `60-69`

```js
for (let i = 60; i <= 100; i++) {
  if (i >= 60 && i <= 69) {
    console.log("For,", i, " you got a D.");
  } else if (i >= 70 && i <= 79) {
    console.log("For,", i, " you got a C.");
  } else if (i >= 80 && i <= 89) {
    console.log("For,", i, " you got a B.");
  } else if (i >= 90 && i <= 100) {
    console.log("For,", i, " you got an A.");
  }
}
```

### 4: Favorite TV Shows

1. Create an Array to hold your favorite TV shows
1. For each show, print to the console a string like:

   ```
   My #1 choice is Person of Interest
   My #2 choice is Battlestar Galactica
   ```

```js
let tvShows = [
  "Kobra Kai",
  "Better Call Saul",
  "Stranger Things",
  "The Boys",
  "Below Deck"
];

let showPreference = 0;

for (let i = 0; i <= tvShows.length - 1; i++) {
  console.log("My #", showPreference + 1, "choice is", tvShows[i]);
  showPreference++;
  if (showPreference === tvShows.length) {
    showPreference = 0;
  }
}
```

### 5: Age Filter

1. Create an Array to hold a list of ages
1. Loop through and log only the ages that are over 21

```js
let age = [16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26];

for (let i = 0; i <= age.length; i++) {
  if (age[i] > 21) {
    console.log(age[i]);
  }
}
```

## Optional Bonus Problems

You don't have to complete these problems. They are only provided as an extra challenge if you are hungary for more practice.

### 1: Change Odd Numbers

Change all **odd numbers** in the Array to their value multiplied by 2:

```js
const numbers = [4, 9, 7, 2, 1, 8];

for (let i = 0; i < numbers.length; i++) {
  if (numbers[i] % 2 !== 0) {
    console.log(numbers[i] * 2);
  } else {
    console.log(numbers[i]);
  }
}
```

## Submission Guidelines

- Cite any relevant sources consulted during your research
- Solve the problems using your own code
- Do not copy and paste solutions from the source material
