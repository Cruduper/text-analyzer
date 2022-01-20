# _{Application Name}_

#### By _**{List of contributors}**_

#### _{Brief description of application}_

## Technologies Used

* HTML
* CSS
* javascript
* jQuery

## Description

_{This is a detailed description of your application. Give as much detail as needed to explain what the application does as well as any other information you want users or other developers to have.}_


## Tests

### Describe: wordCounter()

Test: "It should return 1 if a passage has just one word."
Code:
const text = "hello";
wordCounter(text);
Expected Output: 1

Test: "It should return 2 if the passage has two words."
Code:
const text = "hello there";
wordCounter(text);
Expected Output: 2

Test: "It should return 0 for an empty string."
Code: wordCounter("");
Expected Output: 0

Test: "It should return 0 for a string that is only spaces."
Code: wordCounter("            ");
Expected Output: 0

Test: "It should not count numbers as words."
Code: wordCounter("hi there 77 19");
Expected Output: 2

Test: "It should not count numbers as words."
Code: wordCounter("hi there 77 19");
Expected Output: 2




### Describe: numberOfOccurrencesInText()

Test: "It should return 0 occurrences of a word for an empty string."
Code:
const text = "";
const word = "red";
numberOfOccurrencesInText(word, text);
Expected Output: 0

Test: "It should return 1 occurrence of a word when the word and the text are the same."
Code:
const text = "red";
const word = "red";
numberOfOccurrencesInText(word, text);
Expected Output: 1

Test: "It should return 0 occurrences of a word when the word and the text are different."
Code:
const text = "red";
const word = "blue";
numberOfOccurrencesInText(word, text);
Expected Output: 0

Test: "It should return the number of occurrences of a word."
Code:
const text = "red blue red red red green";
const word = "red";
numberOfOccurrencesInText(word, text);
Expected Output: 4

Test: "It should return a word match regardless of case."
Code:
const text = "red RED Red green Green GREEN";
const word = "Red";
numberOfOccurrencesInText(word, text);
Expected Output: 3

Test: "It should return a word match regardless of punctuation."
Code:
const text = "Red! Red. I like red, green, and yellow.";
const word = "Red";
numberOfOccurrencesInText(word, text);
Expected Output: 3

Test: "If an empty string is passed in as a word, it should return 0."
Code:
const word = "";
const text = "red RED Red!";
wordCounter(word, text);
Expected Output: 0



### Describe: boldPassage()

Test: "It should return a non-matching word in a p tag."
Code:
const word = "hello";
const text = "yo";
boldPassage(word, text);
Expected Output: "<\p>yo</\p>"

Test: "It should return a matching word in a b tag."
Code:
const word = "hello";
const text = "hello";
boldPassage(word, text);
Expected Output: "<\p><\b>hello</\b></\p>"

Test: "It should wrap words that match in \`b\` tags but not words that don't."
Code:
const word = "hello";
const text = "hello there";
boldPassage(word, text);
Expected Output: "<\p><\b>hello</\b> there</\p>"



### Describe: mostUsedWords

Test: "It should return default array values for empty string input"
Code:
const text = "";
mostUsedWords(text)
Expected Output: ["", 0, "", 0, "", 0]

Test: "it should add word and number of instances of that word to first 2 indices of output array for single word input"
Code:
const text = "hello"
mostUsedWords(text)
Expected Output: ["hello", 1, "", 0, "", 0] 

Test: "it should add 2 words and instance count of 1 to first 4 indices of output array for 2 word input"
Code:
const text = "hello there"
mostUsedWords(text)
Expected Output: ["hello", 1, "there", 1, "", 0]

Test: it should add the first 3 words and instance count of 1 to output array for 3+ word input"
Code:
const text = "hello there carl danger"
mostUsedWords(text)
Expected Output: [hello, 1, there, 1, carl, 1]





## Setup/Installation Requirements

* download git repo, then open index.html in your browser

_{Leave nothing to chance! You want it to be easy for potential users, employers and collaborators to run your app. Do I need to run a server? How should I set up my databases? Is there other code this application depends on? We recommend deleting the project from your desktop, re-cloning the project from GitHub, and writing down all the steps necessary to get the project working again.}_

## Known Bugs

* although spaces at the beginning and end are deleted, gives incorect total word count when more than one space is added between words
* if a longer word contains our selected word (i.e. "redo" contains "red), the selected word count still increases even though the words are different.

## License

_{Let people know what to do if they run into any issues or have questions, ideas or concerns.  Encourage them to contact you or make a contribution to the code.}_

Copyright (c) _date_ _author name(s)_