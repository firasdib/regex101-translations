# Translations for regex101

Base your translation off of `english.json`. The keys are the english words, do not touch these. They need to remain identical. If there is a typo or problem, open an issue/inform me and I'll sort it out. Strings may contain placeholders, indicated with `{n}` where `n` is a positive number greater than zero. Do not remove these, but feel free to move them around. Quite often you can figure out what they are inserting (almost always a non-translatable string, such as a number).

When you are finished, just push your changes over here in a new json file with the language name.

**Note: The strings are treated literally, you may not (and need not) use any html tags or entities.** 

## Example

```json
{ 
  "Match found in {1} step(s)": "Match funnen efter {1} steg",
}
```

## Compare languages

I sometimes update the english language table, which means other langauges need to adjust. Here's a tiny snippet that allows you to compare two files and see what keys you are missing, and produces a new combination of both languages.

```js
let english = { a: 'a', b: 'b' };
let anotherLang = { b: 'b2', c: 'c' };

// This creates a new object based off of `english` with the other language overwriting the keys
let combinedLanguage = Object.assign({}, english, anotherLang);

let englishKeys = Object.keys(english);
let anotherLangKeys = Object.keys(anotherLang);

console.log('New language combination', combinedLanguage);

console.log('Missing keys in anotherLang:', englishKeys.filter((key) => anotherLangKeys.indexOf(key) === -1));
console.log('Extra keys in anotherLang:', anotherLangKeys.filter((key) => englishKeys.indexOf(key) === -1));
```
