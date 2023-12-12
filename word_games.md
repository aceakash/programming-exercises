# Word Games

Do one part at a time. Do not look ahead.

<details>
  <summary>Part 1</summary>
  
  ## Part 1

Write a command-line program that asks the user to unscramble a 5-letter word.

When the user runs the program (`./word_games`), a scrambled 5-letter word is shown to them. The program then awaits their answer.

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

Show them 2 unique scrambled words from your list.

They can unscramble in any order, but one at a time.

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

Have the option of reading in the user's preferences (number of words, length of each word) via environment variables

e.g.

```
WORD_COUNT_PER_SESSION=2 WORD_LENGTH=5 ./word_games
```

If a preference is available via an environment variable, don't prompt the user in-program.

</details>
