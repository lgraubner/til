# Add multi command aliases

It's possible to create custom git aliases in a `.gitconfig` file.

```
[alias]
        s = status -s
        co = checkout
        cb = checkout -b
        cl = clone
        ci = commit -m
````

Which can be used like `git s` etc. To add an alias for adding and commiting in one command you have to do the following:

```
        ac = !git add -A && git commit -m
```

Very useful!