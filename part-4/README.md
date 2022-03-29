# Looping in the Shell

The for loop which you will very familiar with can also be used in your shell scripts.

---

## For ... In

An example of an older syntax:

```sh
for num in 1 2 3 4 5; do
  echo $num
done
```

> 💡 Note the use of `do` and `done` around the action you want to take within your loop

Newer versions of Bash have a much nicer syntax:

```sh
for num in {1..5}; do
  echo $num
done
```

Both these examples will produce the same effects.

---

## C Style For Loop (3 expression loop)

This next one will be even more familiar:

```sh
for (( i=1; i<=5; i++ )); do
  echo $i
done
```

> 💡 The double parentheses allows us to use arithmetic expansion and evaluation. You can omit a set of parentheses however this will mean you are unable to use operators such as `<` and `>`. Using the syntax above is a lot cleaner. Bash isn't great with numbers, for reasons that will be covered later.

---

## Exercise:

Create a script that loops through a directory and prints the names of each sub-directory. Feel free to use Google. It's easier than it sounds!

---

## Further learning:

- Read more about for loops in Bash [here](https://www.cyberciti.biz/faq/bash-for-loop/)
- Look into how to create a `while` and a `until` loop
