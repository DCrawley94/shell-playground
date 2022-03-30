# String Manipulation

There are far too many ways of manipulating strings to mention them all here but here are some examples.

---

## Finding the Length of a String

```sh
string="This string is 33 characters long"
length=${#string}
```

---

## String Concatenation

```sh
day=19
week=01
year=1994
dob="My date of birth is $day/$month/$year"
echo $dob
# Prints "My birthday is 19/01/1994"
```

You can technically do something like this instead of using quotes around your variables:

```sh
bday=$day.$month.$year
```

However this leaves you open to unintended results. Please see [this article](https://linuxhint.com/bash_escape_quotes) for a thorough explanation of this.

---

## Extracting Substrings

There is a nice easy syntax for extracting substrings. It follows this pattern: `substring=${string:position}` or `substring=${string:position:length}`.

For example in the case where we know exactly what point we want to start and end we could do the following:

```sh
string=Hello!
slice_second_half=${string:3:6}
echo $slice_second_half
# prints 'lo!'
```

> 💡 Notice that within the curly braces we don't need to use the `$` to access variables.

---

## Regex

Finally we get to `regex`. There are many ways to use regex in a shell script.

You could just use it for conditional checks like so:

```sh
haystack=hayhayhayhayneedlehayhayhayhay

if [[ "$haystack" =~ [needle] ]]; then
  echo "Found the needle!"
else
  echo "No luck :("
fi
```

However this is only scraping the surface!

You can see just how powerful it is when it is combined with other commands:

![Using Regex with other Commands](./images/Screenshot%202022-03-30%20at%2016.23.47.png)

Bit of a contrived example but here you can see the first example where I've used `ls` to view the contents of this repo.

In the second example however I have piped the `stdout` from ls into the `grep` command with uses a regex. In simple terms I have listed all files that start with a 'p'.

`Piping` and `stdin`/`stdout`/`stderr` will be covered later but feel free to do your own research!

---

## Exercise

See if you can make a script that counts how many git repositories you have by checking the contents of your directories.

- **Hint:** The easiest way to check if a directory is a git repo is to see if it has a `.git` directory within it.
- **Hint:** The find command could be useful here 👀
