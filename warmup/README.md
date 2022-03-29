# Aliases

Something you might have noticed about using the command line is that the majority of commands you run are a very small subset of the available commands. For example you may find yourself using `cd` an `ls` regularly.

Admittedly just having to type `cd` is already saving a lot of time. However if you find yourself navigating to the same directories or doing the same commands regularly you can make it even quicker by using an **alias**.

---

## What is an alias

An alias could be described as being a method of overiding Bash commands with new ones. They allow you to customize your terminal experience to suit your needs.

Here's an example. Instead of manually typing out a long `cd` command or repeatedly changing directory until we get to the right place we can define a sort of nickname for a shortcut. This way instead of typing it all out we can just type `reviews` and it'll take us right to where we want to go.

![A Simple Alias](./images/short-alias.png 'A simple alias')

You can also chain as many commands as you like though be careful it doesn't get too complicated. Anymore than a few commands and I'd recommend extracting it into it's own script.

![A more complicated alias](./images/longer-alias.png 'A more complicated alias')

---

## How to create an alias

There a a lot of aliases the come premade for you to use whether you're using linux or macOS. To see a list of current aliases run the command `alias` in your terminal.

If you want to make your own you can define an alias in the terminal like so:

![A temporary alias](./images/temp-alias.png 'A temporary alias')

However this would only last as long as your current shell session. A better option would be to add them to a config file (for example `.bashrc` or `.zshrc`) like so. This way they will be accessible whenever you're using the command line.

![A selection of permanent aliases](./images//zshrc.png 'A selection of permanent aliases')

Have a go at making some a your own!
