- single characters are the building block of regex
- special regex characters must be escaped with a \ backspace
- regex is case sensitive unless you specify with a \i insensitive tag
- regex must be declared with the \g flag to find all occurrences of a search
- Characters can be looked for individually with the | character
  - example: b|i|g
- Characters can also be looked for in a set with square brackets
  - example: [big]
- Characters can be searched for as NOT some set of characters with the ^ character
  - example: [^aeoiu] will return all characters that ARE NOT vowels
- If the ^ hat character is not the first character of the set it will be treated as a character in the search set
- The - minus symbol set's a range of letters or numbers
  - example: [a-d] searches for letters a through d
  - example: [1-8] searches for numbers 1 through 8
- You can buttress search ranges next to each other
  - example: [a-z1-9] will search for a through z or 1 through 9
- If you want to find something but not replace a part of it that is 'ahead' or forward you can use the look ahead assertion
  - example: to replace the first `>` in only the patterns that have two `> >` you can search `> (?= >)` and only the first one will be replaced.
- If you want to replace a new line break you can use `\n` as the new line character

  - example: you want to get rid of whitespace between </tag> ending tags you can search `</tag>\n`

- If you want only a beginning of a word and not it's potential group in a series you can use the `\b` word escape assertion

  - example: to find the word `log` only in the phrase `this is a catalog of a blog's logs you can search `\blog`and it will only find`logs`.

- If you want to match just the start of a string you can use the ^ hat
  - example: apple\napple \n is a new line you should use the \m multiline flag
- If you want to find digits you can use \d
- If you want to find anything 'but' digits you can use the negation assertion \D
- To replace white space characters you can use \s
- \b represents a word boundary which is any non-word character
- word characters are letters, numbers and underscores
- the \w word class finds words that have word boundaries

  - example: Pine-apple Juice would have three matches for \w+ because it is a word character followed by as many word characters as possible before a boundary.

- You can validate your forms with the following input types `text, tel, email, url, password, search`
- The browser automatically includes `/` forward slashes for unicode as well as `^` hat character and `$` dollar sign for start and end of line
