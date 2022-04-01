# Shell Functions

## Defining a Function

Again this syntax will be quite familiar to you:

```sh
function function_name {
  commands...
}
```

You can also do it like this:

```sh
function_name () {
  commands...
}
```

---

## Function Invocation

When it comes to actually invoking the function it's as simple as just referencing it:

```sh
hello_world () {
   echo 'hello, world'
}

hello_world
```

---

## Return Values

It's worth mentioning that unlike other programming languages you **cannot** return a value when a function is called. When a function completes, it's return value is the **return status** on the last command in the function body. This is either `0` for success or a non-zero positive number in the `1-255` range.

The return **status** can be specified using the **return keyword** and accessed with the variable `$?`. This terminates the function and can be thought of as the exit status.

---

## Passing Arguments

Arguments can be passed to a function by simply putting them right after a function name separated by a space. It's good practice to double-quote any arguments to avoid parsing issues. Especially if an argument has spaces in it!

Any arguments passed to a function can be accessed with a dollar sign an a number. `$1` for the first argument, `$2` for the second etc.

```sh
function say-hello () {
  firstname="$1";
  lastname="$2";

  echo "Hello $1 $2";
}

say-hello "Duncan" "Crawley"
```

It's good practice to rename any passed arguments as it makes your code much clearer to read!

---

## Exercise

In the the provided file create a function that echos a greeting message using any passed arguments.
