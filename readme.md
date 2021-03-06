# [DoggoTranslator (core) :dog:](https://gabbersaurus.github.io/DoggoTranslator/)
> The universal doggo translator

I made this a while ago for fun in Vue with ES6 JavaScript. Later, I made the translator standalone and this repository is for just the core translator. If you don't know what this is all about you should read [this](http://knowyourmeme.com/memes/doggo) page.
The reason I didn't release it back then because it is still missing alot of translations and the code isn't that clean. If you have suggestions for translations, see the `How to contribute` section.

## How to install
Using npm:
```bash
npm install doggotranslator
```

## Example
Translating a sentence

```js
import DoggoTranslator from 'doggotranslator';

//Create a new translator instance set to English
let doggoTranslator = new DoggoTranslator('en');

//Translating english to doggo speak
let englishToDoggo = doggoTranslator.translateSentence('Hi friend!', false);
console.log(englishToDoggo); //Hi fren!

//Translating doggo speak to english
let doggoToEnglish = doggoTranslator.translateSentence('Hi fren!', true);
console.log(doggoToEnglish); //Hi friend!
```

## API
When creating a new DoggoTranslator instance, you must set the language by passing the language to the constructor.

**new DoggoTranslator({string} language)**

The following methods are available on a DoggoTranslator instance:

**translateSentence({string} sentence, {bool} reversed)**

This returns a translated string from the given sentence.
When reversed is set to false, it translates from the language in the DoggoTranslator instance to doggo speak.
When reversed is set to true, it translates from doggo speak to the language set in the DoggoTranslator instance.

**getLanguages()**

This returns an array with the languages as strings.

**setLanguage({string} language)**

This sets the language on the DoggoTranslator instance to the given language. The language name should be the same as in the array given by `getLanguages()`. If the language doesn't exist it defaults back to `en` and logs an error.


## Todo
* Add more translation possibilities and making the translating smarter.
* Maybe remove the error when a language is not found when node is running in production

## How to contribute
If you want to add features, improve some code or add translations you are more than welcome to submit a Pull Request to this repo.
If you don't know what to do, follow [this](https://github.com/MarcDiethelm/contributing/blob/master/README.md) guide.

If you have suggestions for features or translations and don't know how to program or git, you can create an issue on this Github repository.

## License
This application is released under the [MIT license](https://github.com/Gabbersaurus/DoggoTranslatorCore/blob/master/LICENSE).