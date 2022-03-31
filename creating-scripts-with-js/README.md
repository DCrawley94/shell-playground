# Creating a package

So you've got a great idea for something in JavaScript (or TypeScript..!) that will revolutionise your working process. This could be something that will install a project (see: section 2 of the [fun-callback-heaven](https://github.com/northcoders/fun-callback-heaven) sprint), or something more useful like serving you a dad joke or your Pokemon of choice.

To create and install something globally on your machine, first create your project and make a function that does something.

A nice example is a project that will print `Hello, <name>!` When `printName sam` is written in the CLI.

Create a project as normal, but call it the command you want it to type in, so in this case, `printName`.

At the top of the file, we need to tell our project what we are using to run our project. We do this using a `shebang` - `#!` - followed by the path to the end program search path and a `node` interpreter. Read more about it [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#hashbang_comments):

```js
#!/usr/bin/env node
```

Let's make a function in `index.js` that logs a name in the console when passed a name:

```js
const printName = (name) => console.log(`Hello, ${name}!`);
```

Now we've all used `module.exports` before, but did you know you can attach an _invoked_ function to it? But first we need to get our `name` variable from the CLI. We do this using `process`:

```js
const name = process.argv[2];
```

_What are process.argv[0] and [1]? Have a look!_

We can put as many arguments as we want in the command and access them using `process.argv`.

_NB - This will not work if you need your Current Working Directory (CWD) - how do we get that?_

Now attach your invoked function to `module.exports`:

```js
module.exports = printName(name);
```

So our `index.js` file has 4 lines of code:

```js
#!/usr/bin/env node

const printName = (name) => console.log(`Hello, ${name}!`);

const name = process.argv[2];

module.exports = printName(name);
```

Now we need to make it executable, using the old warhorse, `package.json`!

Read more about package.json [here](https://docs.npmjs.com/cli/v7/configuring-npm/package-json)

This is done simply by adding a "bin" property to our `package.json`:

```json
"bin": "./path/to/index.js"
```

We now need to package it up! If we run `npm pack`, the project will be compressed and zipped up into a `.tgz` file with the following naming convention: <name>-<version>.tgz, where `name` and `version` are taken from the package.json.

Install it globally:

```bash
npm install -g ./<installationfile>.tgz
```

Now run it in your terminal!

```bash
printName sam

# Hello, sam!
```

Think about other things we could use this for...

Creating projects - https://github.com/northcoders/fun-callback-heaven
Showing us a dad joke - https://rapidapi.com/KegenGuyll/api/dad-jokes/ (needs a key etc...)
Our choice of pokemon - https://pokeapi.co/
A DICE ROLLER...?!
