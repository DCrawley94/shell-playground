# Maths

If you were to run this command in the shell what would you expect to see?

```sh
echo 1 + 1
```

- `2` ?
- `"11"` ?

Give it a go and see what happens

---

As you might have realised arithmetic is not quite as simple other programming languages such as JavaScript!

In order to see a more logical output you would need to use syntax like this:

```sh
echo $((1 + 1))

# OR

echo $[1+1]

# OR

expr 1 + 1
```

If you wanted to save the result of an arithmetic expression to a variable you could also use the following:

```sh
let a=5+4

# OR

a=$( expr 5 + 4 )
```

Personally I would recommend using the `(( maths...))` syntax. The double parenthesis allows many mathematic operations and is also useful in if statements as shown below.

```sh
x=5

if (( x = 5 )); then
  echo "This number is the number 5"
fi
```

> 💡 It's worth noting noting that `$(( ))` and `(( ))` are two different things. The first is **arithmetic expansion** which has an `output`. The second is the **compound command** which does not have an output (though it does have an exit code which will be covered later). Internally they do both follow the same rule though and are both suitable for arithmetic expressions!

---

## Exercise

In the provided file write a conditional statement that check whether the number stored in the variable `x` is odd or even. Does it still work when you change the value?
