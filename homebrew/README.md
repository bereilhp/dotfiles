## Homebrew

Homebrew packages are managed with the Brewfile in `homebrew/Brewfile`.

Install everything from the Brewfile:

```sh
brew bundle --file homebrew/Brewfile
```

Update the Brewfile from the packages currently installed on this Mac:

```sh
brew bundle dump --file homebrew/Brewfile --force
```

Check whether the installed packages match the Brewfile:

```sh
brew bundle check --file homebrew/Brewfile
```

Clean up packages that are not listed in the Brewfile:

```sh
brew bundle cleanup --file homebrew/Brewfile
```

If `brew bundle check` says it cannot satisfy the Brewfile dependencies, list the missing packages with:

```sh
brew bundle check --file homebrew/Brewfile --verbose
```

Install the missing packages with:

```sh
brew bundle install --file homebrew/Brewfile
```

If you are already inside the `homebrew` directory, use `--file Brewfile` instead.
