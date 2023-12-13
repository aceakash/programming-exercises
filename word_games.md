# Word Games

Do one part at a time. Do not look ahead.

<details>
  <summary>Part 1</summary>
  
  ## Part 1

Write a command-line program that asks the user to unscramble a 5-letter word.

When the user runs the program (`./unscramble`), a scrambled 5-letter word is shown to them. The program then awaits their answer.

If correct, the program acknowledges that and exits.

If incorrect, it shows the correct word and exits.

Hard-code the following list of words in the program to randomly pick from: `pound, trice, hired, comma, logic`

</details>

<details>
  <summary>Part 2</summary>
  
  ## Part 2

Modify the program to pick a 5-letter word at random from a word list. You can use the provided `words.txt`.

</details>

<details>
  <summary>Part 3</summary>
  
  ## Part 3

Modify the program to allow the user to attempt two different words.

Show them 2 unique scrambled words from your list, one at a time.

After each attempt, let the user know if their answer matched any of the words.

</details>

<details>
  <summary>Part 4</summary>
  
  ## Part 4

When the program starts, ask the user to specify the number of words they want to play, and show them those many words (instead of 2, as previously implemented)

</details>

<details>
  <summary>Part 5</summary>
  
  ## Part 5

When the program starts, ask the user to specify the length of each word they want to play and only show words of that length (instead of 5, as previously implemented)

</details>

<details>
  <summary>Part 6</summary>
  
  ## Part 6

Have the option of reading in the user's preferences (number of words, length of each word) via command-line args

e.g.

```
./unscramble --word-count 2 --word-length 5
```

If a preference is specified via a command-line arg, don't prompt the user in-program.

</details>

<details>
  <summary>Part 7</summary>
  
  ## Part 7

Ask the user if they want a casual or timed session.

If it's a timed session, for every successful solve measure how long it took them, and report it back.

This preference can also be specified via command line arguments,.

```
./unscramble --mode {casual|timed}
```

</details>

<details>
  <summary>Part 8</summary>
  
  ## Part 8

It's getting too tedious for users to answer the preference questions everytime.

They would prefer to have defaults that can be overridden.

Change the program so that running it without any command line args uses default values and does not ask any questions of the user in this regard.

Think of the user experience, especially those users who have been used to the questions.

</details>
