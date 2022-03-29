# Creating and Running a Shell Script

A unix shell is a command line interpreter that provides a command line ui for unix-like operating systems. The shell is both an interactive command language (i.e. running commands in the terminal) and a scripting language. Examples of different shells include the Bourne shell (`sh`), Bourne-Again shell (`bash`), KornShell (`ksh`) and Z shell (`zsh`) though there are many others.

## Writing a shell script

A shell script is technically just a text file that contains one or more commands. According to Google's [Shell Style Guide](https://google.github.io/styleguide/shellguide.html) executable files should have no extension (though sometimes you'll see files with a `.sh` extension).

It is good practice to start your file with a ✨ _shebang_ ✨ (no really!). The shebang consists of a number sign and an exclamation point (`#!`), followed by the full path to your chosen interpreter. Again the Shell Style Guide states that executables must start with `#!/bin/bash` and is recommend for compatibility between machines but you can use others should you choose.

One final thing, in order to run the file you must use the change mode command (`chmod`) and make it executable like so:

```sh
chmod u+x YOUR_FILE_HERE
```

---

## Exercise 1

- Create a script in the `hello-world` file that will print the message "Hello World!" and run it. A shell script can be run by typing the file path into your terminal.
