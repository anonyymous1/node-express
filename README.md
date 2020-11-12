# node-express

Notes:

### Creating Node
1. You go to your `Github` and create a `Repo`.
2. Once you create that `Repo` go into your terminals to `clone` it locally.
3. Once you `clone` you repo.
4. Be sure to go into your `repo folder` to start the process.
5. Two options you have are `npm init` which will ask you details on your project if you want to be more descriptive, or `npm init -y` which will default all the settings to yes and blank.
Questions it will ask for `npm init`: ( It will also show you what is default if you hit enter. )
```text
{
  "name":
  "version": "1.0.0",
  "description":
  "main": "index.js",
  "scripts": {
    "test": 
  },
  "repository": {
    "type": "git",
    "url": 
  },
  "author": 
  "license": "ISC",
  "bugs": {
    "url": 
  },
  "homepage":
}
```
6. If you did the previous steps correctly, you should be able to `ls` to see you now have a `package.json` file along with you `README.md` file.
7. To check what is in the `package.json` file, type in `cat package.json` in your terminal. This will display the content.
8. Be sure to check what you `"main"`. Your `.js` file mus have that same name.
9. Now if you try to write `code` that will usually show up in the console, you can simple type `node index.js` (name if your .js file) and it will show in your terminal.
10. Go ahead and type in `console.log('Hello')` into your `index.js`. Then in your terminal type `node index.js`.

Good Job! You did it!

### Importing Exporting

When creating functions in other `.js` files, you must be sure to export them to be used outside that file. In this case my `.js` file is called `myModule.js`
For example:
```js
const beBasic = () => "That's so fetch!";

function add(num1, num2) {
    return num1 + num2;
}

function subtract (num1, num2) {
    return num2 - num1;
}

module.exports = { // functions you want to export go here.
    beBasic, 
    add, 
    subtract
}
```

Now when called in other `.js` files, you can use the following to use.
```js
const {add, subtract, beBasic} = require ('./myModule') //This line pulls the functions from our other .js file (myModule.js)

let name = 'Ruben Cedeno';
console.log(name);

function printName (person) {
    return `hello, ${person}`;
}

console.log(printName(name));
console.log(beBasic());
console.log(add(5,50));
console.log(subtract(10,20));
```
### Now once again check your terminal using node. You're Done!