# Creating and Using Shell Variables

## Variable Declaration

Variable declaration in the shell is quite simple and is done like so:

```sh
hello="world"
```

By convention environment variables such as USER, PATH, HOME etc. are capitalized. Any other variable names should be lowercase. The convention will help you avoid accidentally overwriting environmental and internal variables.

> 💡 Notice that there is no space before or after the `=`. This is due to the way the Bourne shell (and it's variants) interpret commands.

```sh
var =23
# This is interpreted as the 'var' command with '=23' as an argument
var= 23
# An assignment followed by a command name
var = 23
# 'var' command with '=' and '23' as arguments. A good way to visualize this is with the echo command.
```

![Variable declaration errors](./images/variable-declaration-errors.png 'An example of common errors when declaring a variable')

---

## Using Variables

Once declared a variable can be accessed by prefixing it's name with a `$`.

```sh
name="Duncan"

echo $name
# Prints Duncan to the terminal when run
```
