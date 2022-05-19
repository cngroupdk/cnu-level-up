# CNU Level 1: Macbook setup

**Macbooks** are excellent machines for frontend developers. Out of the box, they provide support for UNIX command line environment (shell) and allow installation of all major browsers (**Chrome**, **Firefox** & **Safari**). They also provide a platform for native **iOS** development, which is necessary for technologies like **ReactNative**. By installing the essential tool of this platform, `xcode`, you gain access to the **iOS Simulator**, which can be used to preview your web apps on any type of **iPhone** or **iPad**.

[TL;DR](#tldr)

## 1. Installing software onto your Mac

Common desktop apps like browsers can be easily installed via the Apple's **App Store** or the CN-provided **Trubadix** app. In general, use those apps to search for anything you need as they provide the most safe way to install software. Of course, the traditional way of downloading and installing programs manually works as well.

## 2. Terminal - the command line app

Frontend development requires basic knowledge of working in the command line. On **Windows**, you may have already used the **Command Prompt** or the **PowerShell**. On **Mac** or **Linux**, the command line environment is called a **shell** and the app through which you can access the shell is called a **terminal**. Mac provides a default terminal application out of the box, but there are much better alternatives out there.

> For the sake of simplicity, you can consider the words _terminal_, _command line_, _shell_ or _command prompt_ to mean the same thing - a screen where you can type-in and execute commands.

For a beginner, the [iTerm2](https://iterm2.com/downloads.html) is the best choice. It comes with lots of bells and whistles and allows for some pretty advanced configurations. However, you do not need to overwhelm yourself with the options and adjusting the font family and size maybe the only configuration you will need.

_Please note that installing a terminal app is not required and that you can handle everything command-line-related from within the built-in **VS Code** terminal. There's nothing wrong of using only this terminal as it provides you with the same environment as a standalone application would. Although a good terminal and command-line knowledge empowers you to do many cool things, only few basic commands are essential at the beginning. For these reasons, a terminal built into your editor should suffice._

> A pro tip - you don't need to re-enter previously used commands each time you want to use them since every terminal app has a history log that you can navigate through. The most simple way is to use the arrow-up key repeatedly on an empty command line to access previous commands. A better way, however, is to press `Ctrl+R` keys and to start typing beginning of your command. This would lead to a matching command from your history being shown.

> For a beginner-friendly introduction to terminals and shells, we recommend [this article](https://www.freecodecamp.org/news/command-line-for-beginners/).

## 3. Homebrew - the package manager

Although the preferred way to install software on Macs is via the **App Store**, many essential developer tools are not available there, nor can they always be easily downloaded and installed manually. The `Node JS` environment is a good example of this. In order to install these tools, you need to use a special program - a package manager. Luckily, there's an excellent package manager available for **Mac** called **Homebrew**. It is installed- and operates from- the command line.

To install [Homebrew](https://brew.sh/), open your terminal and paste and run the following command:

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

You can verify successful installation by typing a command to install something, for example:

`brew install wget`

_Please note, you don't need to overwhelm yourself by installing and exploring tons of tools at once. While it's good to have **Homebrew** installed from the start, add additional packages only once you need them._

## 4. `xcode` and `xcode tools`

In order to develop in **ReactNative** and/or to use the **iOS Simulator** app, the `xcode` environment has to be installed from the **App Store**. However, **it's unlikely you would need it at this stage** and only install it if instructed to do so or if you really want to check it out. Also keep in mind that the installation is several gigabytes large.

What you will needed from the start, however, are the `xcode command line tools`. At the very least, `git` would not work without these. **[`xcode tools`](https://www.maketecheasier.com/install-command-line-tools-without-xcode/) should be installed automatically with Homebrew!** If you type `git --version` in your terminal and get back a version number, you should be fine already. If you get back `command not found`, you should install `xcode-tools` from the terminal:

`xcode-select --install`

## 5. `nvm`, `node` & `npm`

`Node JS` is an essential tool which powers the modern frontend development. While you can download and install `node` manually using an official installer, it is not actually the recommended way. In practice, projects you encounter will differ greatly in their required version of `node`, but you can only have one version of `node` installed on your system. To combat this problem, tools like `nvm` must be used. They allow you to pre-install any number of node versions and then have only one "active".

`nvm` can be installed via Homebrew: `brew install nvm`.

Before you can start using `nvm`, you must tell your shell how it should interpret the `nvm` command. This is a tricky part, as you must locate the configuration file of your shell and open it in your editor. If you don't know what a shell is and haven't mess around your system, the file you are looking for is most likely `/Users/myName/.bashrc`. If you already have `zsh` installed (section #6), the file would instead be `.zshrc`. Once you have the file, append the following at the very bottom:

```
export NVM_DIR=~/.nvm
source $(brew --prefix nvm)/nvm.sh
```

Don't be afraid, ask for help, if needed ;-)

After installation and configuration, you can verify if `nvm` is working with: `nvm --version`.

To list currently installed `node` versions, use: `nvm ls`.

To add a particular version: `nvm install 10.16.0`.

A full installation guide [can be found here](https://tecadmin.net/install-nvm-macos-with-homebrew/).

> Projects usually have a special file, `.nvmrc`, which contains the required version. Whenever you switch your terminal to such project's directory, use the command `nvm use` to activate the version from the `.nvmrc` file. `nvm` would warn you if that version is not installed, all you need to do in such case is to add it with the command mentioned above.

> Please note that `nvm use` **does not work** on Windows.

**NPM**

`npm` is package manager for `node` (just like Homebrew is for Mac). It allows you to install libraries and tools needed for development and is really the driving force of the whole `node` ecosystem. It comes automatically with `node`.

Every project contains a `package.json` file which lists all the packages that the project needs. These are installed with `npm install` command, which creates a local `node_modules` folder where the downloaded packages are placed. However, you may still want to install certain tools globally, so that those can be used across all your projects. One such tool is `yarn`, which is often the preferred command used to build your projects. To install it globally, use `npm install -g yarn`. The `-g` switch is what determines that something is installed and accessible globally and not in a local `node_modules` folder.

A word of caution - whenever you install something globally with `npm`, it is installed **only for the currently active version of `node`**. Thus, if you use `nvm` to switch to a different version and want to use the same global tool (like `yarn`), you must install it globally again.

## 6. `zsh` and `oh-my-zsh`

_Using these tools is entirely optional and only makes sense if you would like to spend more time in your terminal._

When you open a terminal and type in a command, it would get executed thanks to a command-line interpreter. In UNIX-based world of **Mac** and **Linux**, this interpreter is called a **shell**. **Mac** comes with a pre-installed default shell called `bash`, which allows you to do everything you may ever need to do in a shell. However, there are actually many different shells to choose from and switching from `bash` to something else can provide you with some niceties that make everyday life in the command line easier.

`zsh`, together with its extension `oh-my-zsh`, is a version of shell which maintains lots of popularity among frontend developers. The extension adds many useful tools, which come as configurable plugins. There are many plugins to choose from, but for the start, `git` and `wd` can provide a nice productivity boost.

> For a beginner-friendly introduction to terminals and shells, we recommend [this article](https://www.freecodecamp.org/news/command-line-for-beginners/).

**Installation**

You can install `zsh` via the good old Homebrew: `brew install zsh`.
After the installation, **quit your terminal app and open it again**. If everything went well, you should now have the terminal pre-loaded with `zsh` instead of `bash`. Chances are, you won't spot any difference 😃.

[Adding oh-my-zsh](https://ohmyz.sh/#install) is done via the following command:

`$ sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`

After installation, open the file `.zshrc` from your home folder (i.e. `/Users/myName/.zshrc`) and navigate to the line which starts with `plugins=(`. The `git` plugin should be enabled by default, append `wd` after it, so that the line looks like this:
`plugins=(git wd)`.

Save the file and quit and reopen the terminal.

<!-- **GIT plugin in `zsh`**

TBA

**WD plugin in `zsh`**

TBA -->

## 7. Code editor

This is also totally up to you. The most of our developers recommend [VS Code](https://code.visualstudio.com/) but you can also choose from vast number of other editors (vim, Atom, Webstorm...)

If you choose **VS Code** here are some useful VS Code plugins:

- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
- [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
- [Live Share Extension Pack](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare-pack)
- [Peacock](https://marketplace.visualstudio.com/items?itemName=johnpapa.vscode-peacock)
- [indent-rainbow](https://marketplace.visualstudio.com/items?itemName=oderwat.indent-rainbow)
- [change-case](https://marketplace.visualstudio.com/items?itemName=wmaurer.change-case)

---

## TL;DR

### 1. `Homebrew`

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### 2. Terminal (`iTerm2`)

```
brew install --cask iterm2
```

### 3. `zsh` and `oh-my-zsh`

Install: zsh:

```
brew install zsh
```

Install oh-my-zsh:

```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Add GIT and WD plugin in `zsh` by adding to the file `~/.zshrc`

```
plugins=(git wd)
```

### 4. `node`, node version manager (`nvm`/`fnm`), node package manager `npm`/`yarn`

Install nvm:

```
brew install nvm
```

Append at the end of file `~/.zshrc`

```
export NVM_DIR=~/.nvm
source $(brew --prefix nvm)/nvm.sh
```

Install latest node:

```
nvm install node
```

### 5. Text editor (`VS Code`)

```
brew install --cask visual-studio-code
```

- Plugins: ESLint, Prettier, GitLens

# Cheatsheets

- [Mac shortcuts cheatsheet](https://support.apple.com/en-us/HT201236)
- [VS Code cheatsheet](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf)
- [Terminal cheatsheet](./cheatsheets/terminal.md)
