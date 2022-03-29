# Conditional Execution

Just like other programming languages you can use conditional statements in Shell scripts.

For example your plain `if` statement:

```sh
if [[ expression ]]; then
  "do something..."
fi
```

> 💡 Note the inclusion of `then` before the statement you wish to execute. Also you must close an if statement with `fi`.

---

There are also `if-else` statements:

```sh
if [[ expression ]]; then
  "do something..."
else
  "do something else..."
fi
```

> 💡 Technically you don't need double square brackets for your condition. However it is recommend when writing for `bash`. If it needs to work for different shells then single square brackets should be used. A detailed (but dense) explanation can be found [here](http://mywiki.wooledge.org/BashFAQ/031).

---

You are also able to use else if and switch statements. I encourage you to look up how to write these if you want to learn how!

---

## Using `&&` and `||`

It's worth mentioning that you can use both the `&&` and `||` operators in a similar way to their use in JavaScript. They can be used in conditions and also to conditionally run commands.

```sh
cd dir && touch file.js
# In the first case if it's possible to 'cd' into dir then it will attempt to create the file
cd dir || touch file.js
# If the 'cd' command is successful then no file will be made. If it is not successful then a file will be created
```

---

## Exercise

Create a script that will conditionally render different variables. Also have a go at using the `&&` an `||` operators.
