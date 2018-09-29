# ~~Mathias’s~~ Bud's dotfiles


![Screenshot of my shell prompt](https://i.imgur.com/EkEtphC.png)

## Installation

**Warning:** If you want to give these dotfiles a try, you should first fork this repository, review the code, and remove things you don’t want or need. Don’t blindly use my settings unless you know what that entails. Use at your own risk!

### Using Git and the bootstrap script

You can clone the repository wherever you want. (I like to keep it in `~/Projects/dotfiles`, with `~/dotfiles` as a symlink.) The bootstrapper script will pull in the latest version and copy the files to your home folder.

```bash
git clone https://github.com/mathiasbynens/dotfiles.git && cd dotfiles && source bootstrap.sh
```

To update, `cd` into your local `dotfiles` repository and then:

```bash
source bootstrap.sh
```

Alternatively, to update while avoiding the confirmation prompt:

```bash
set -- -f; source bootstrap.sh
```

### Use VSCode settings

Make a symlink between our files and VSCode's User settings

_https://pawelgrzybek.com/sync-vscode-settings-and-snippets-via-dotfiles-on-github/_

ln -s /Users/budparr/vscode/settings.json /Users/budparr/Library/Application\ Support/Code/User/settings.json
ln -s /Users/budparr/vscode/keybindings.json /Users/budparr/Library/Application\ Support/Code/User/keybindings.json
ln -s /Users/budparr/vscode/snippets/ /Users/budparr/Library/Application\ Support/Code/User/snippets



### Specify the `$PATH`

If `~/.path` exists, it will be sourced along with the other files, before any feature testing (such as [detecting which version of `ls` is being used](https://github.com/mathiasbynens/dotfiles/blob/aff769fd75225d8f2e481185a71d5e05b76002dc/.aliases#L21-26)) takes place.

Here’s an example `~/.path` file that adds `/usr/local/bin` to the `$PATH`:

```bash
export PATH="/usr/local/bin:$PATH"
```


### Sensible macOS defaults

When setting up a new Mac, you may want to set some sensible macOS defaults:

```bash
./.macos
```

### Install Homebrew formulae

When setting up a new Mac, you may want to install some common [Homebrew](https://brew.sh/) formulae (after installing Homebrew, of course):

```bash
./brew.sh
```

Some of the functionality of these dotfiles depends on formulae installed by `brew.sh`. If you don’t plan to run `brew.sh`, you should look carefully through the script and manually install any particularly important ones. A good example is Bash/Git completion: the dotfiles use a special version from Homebrew.


### Save pass phrase in macOS keychain

these are modified to update the .profile changes for later versions

[Sign your commits on GitHub with GPG](https://medium.com/@timmywil/sign-your-commits-on-github-with-gpg-566f07762a43)
[https://gist.github.com/bmhatfield/cc21ec0a3a2df963bffa3c1f884b676b](https://gist.github.com/bmhatfield/cc21ec0a3a2df963bffa3c1f884b676b)

update profile: https://github.com/robbyrussell/oh-my-zsh/issues/6106#issuecomment-309528254



## Original Author

| [![twitter/mathias](http://gravatar.com/avatar/24e08a9ea84deb17ae121074d0f17125?s=70)](http://twitter.com/mathias "Follow @mathias on Twitter") |
|---|
| [Mathias Bynens](https://mathiasbynens.be/) |
