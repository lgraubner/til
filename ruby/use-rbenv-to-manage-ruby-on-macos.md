# Use rbenv to manage Ruby on MacOS

Manage Ruby versions on MacOS via [rbenv](https://github.com/rbenv/rbenv). Especially if there are permission problems installing gems don't mess with the systems Ruby installation.

```bash
brew update
brew install rbenv
. ~/.zshrc # reload shell
rbenv init
rbenv install 2.5.3
rbenv local 2.5.3
```

## Resources

[https://stackoverflow.com/questions/29932409/bundle-command-not-found-mac/32190234#32190234](https://stackoverflow.com/questions/29932409/bundle-command-not-found-mac/32190234#32190234)
