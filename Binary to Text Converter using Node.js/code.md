# Binary to Text Converter using Node.js

This is a binary converter to a text string. I am using Node.js for this project.

## Installation Check

To check if Node.js and npm are installed, run:

```bash
node -v
npm -v
````

## Code

```javascript
const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout
});

function User_Value(ask) {
  if (!ask) {
    console.log("Don't give me empty input");
    return;
  }

  let result = "";
  for (let i = 0; i < ask.length; i++) {
    const char = ask[i];
    const ascii = char.charCodeAt(0);
    const binary = ascii.toString(2);
    result += binary + " ";
  }
  console.log(result);
}

rl.question("Please give me a binary string :)\n", (answer) => {
  User_Value(answer);
  rl.close();
});
```

To run the script:

```bash
node binaryConverter.js
```

---

## Notes on this code (Step by Step)

1. Create a function.
2. Set a prompt to get user input.
3. Create an `if` statement to check the value.
4. Create a loop to go through the user's input.
5. Convert each character to ASCII using the `charCodeAt(0)` method and store it in a variable called `ascii`.
6. Convert the ASCII value to binary and store it in a variable called `binary`.
7. Add the binary value to the result.
