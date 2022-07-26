_Full Stack Web Development Track_

# Development Environment Setup (Mac)

Open your **terminal.app** or [iTerm2.app](https://iterm2.com/)

> press `COMMAND+SPACE` keys, type `terminal.app`, press `return` to launch

Install the XCode Command Line tools:

```
xcode-select --install
```

> If you get an error saying the command line tools are already installed you can proceed with the instructions

Install [Homebrew](https://brew.sh/) with the following command:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

**Close and Restart your terminal**

## Install development applications with `brew`

```
brew install curl git node@16
brew tap "homebrew/cask"
brew install --cask visual-studio-code postman postico
```

## Run VS Code

From the terminal, you can open VSCode with the command `code`.

You can also open a project folder by providing the path as input to the command:

```
code <path/to/ctp-project>
```

## Install VS Code Extensions

Install the following extensions:

- ESLint
- DotENV
- ES7 React/Redux/React-Native/JS snippets
- Live Share (this will install two packages)
