# Hadi's dotfiles

Forked [Mathias Bynens'](https://github.com/mathiasbynens/dotfiles).

![prompt screen shot](https://igcdn-photos-h-a.akamaihd.net/hphotos-ak-xaf1/t51.2885-15/e35/c71.0.307.307/11821719_1607065079554863_1490092418_n.jpg)

## Prerequisites

### Homebrew
`ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

### RVM
`curl -sSL https://get.rvm.io | bash -s stable --ruby`

Add the following to `~/.extra`
```
# RVM
source ~/.rvm/scripts/rvm
```

## Installation

**Warning:** If you want to give these dotfiles a try, you should first fork this repository, review the code, and remove things you do not want or need. Do not blindly use my settings unless you know what that entails. Use at your own risk!

### Using Git and the bootstrap script

You can clone the repository wherever you want. (I like to keep it in `~/projects/dotfiles`, with `~/dotfiles` as a symlink.) The bootstrapper script will pull in the latest version and copy the files to your home folder.

```bash
git clone https://github.com/mathiasbynens/dotfiles.git && cd dotfiles && source bootstrap.sh
```

To update:

```bash
source bootstrap.sh
```

Alternatively, to update while avoiding the confirmation prompt:

```bash
set -- -f; source bootstrap.sh
```

### Git-free install

To install these dotfiles without Git:

```bash
cd; curl -#L https://github.com/mathiasbynens/dotfiles/tarball/master | tar -xzv --strip-components 1 --exclude={README.md,bootstrap.sh,LICENSE-MIT.txt}
```

To update later on, just run that command again.

### Specify the `$PATH`

If `~/.path` exists, it will be sourced along with the other files, before any feature testing takes place.

Here is an example `~/.path` file that adds `/usr/local/bin` to the `$PATH`:

```bash
export PATH="/usr/local/bin:$PATH"
```

### Add custom commands without creating a new fork

If `~/.extra` exists, it will be sourced along with the other files. You can use this to add a few custom commands without the need to fork this entire repository, or to add commands you do not want to commit to a public repository.

My `~/.extra` looks something like this:

```bash
# Git credentials
# Not in the repository, to prevent people from accidentally committing under my name
GIT_AUTHOR_NAME="Mathias Bynens"
GIT_COMMITTER_NAME="$GIT_AUTHOR_NAME"
git config --global user.name "$GIT_AUTHOR_NAME"
GIT_AUTHOR_EMAIL="mathias@mailinator.com"
GIT_COMMITTER_EMAIL="$GIT_AUTHOR_EMAIL"
git config --global user.email "$GIT_AUTHOR_EMAIL"
```

You could also use `~/.extra` to override settings, functions and aliases from my dotfiles repository.

### Sensible OS X defaults

When setting up a new Mac, you may want to set some sensible OS X defaults:

```bash
./.osx
```

### Install Homebrew formula

When setting up a new Mac, you may want to install some common [Homebrew](http://brew.sh/) formula (after installing Homebrew, of course):

```bash
./brew.sh
```

### Sublime Packages

I found these packages highly useful. Simply install the Package Control for Sublime using the following command or proceed with the installation described [here](https://packagecontrol.io/installation):

Package Control Installation
```
import urllib.request,os,hashlib; h = 'eb2297e1a458f27d836c04bb0cbaf282' + 'd0e7a3098092775ccb37ca9d6b2e4b7d'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

Useful Packages:
`AdvancedNewFile, Alignment, All Autocomplete, ApplySyntax, BracketHighlighter, Case Conversion, Cucumber, Gherkin (Cucumber) Formatter, GitGutter, MarkdownEditing, MarkdownTOC, Pretty JSON, RSpec, SideBarEnhancements, Swift, Theme - Spacegray`

You may find these [MarkdownEditing User Settings](init/Markdown.sublime-settings) user settings helpful.

### Xcode

These are my preferences using Xcode IDE. Feel free to configure them however you prefer.

#### Layout
[Source Code Rro Font](https://github.com/adobe-fonts/source-code-pro)

[SpaceGray Theme](https://github.com/zdne/spacegray-xcode)

#### Package Manager and Useful Packages
[Alcatraz](http://alcatraz.io)

`curl -fsSL https://raw.githubusercontent.com/supermarin/Alcatraz/deploy/Scripts/install.sh | sh`

[VVDocumenter-Xcode](https://github.com/onevcat/VVDocumenter-Xcode)

[MCLog](https://github.com/yuhua-chen/MCLog)

[GitDiff](https://github.com/johnno1962/GitDiff)

### Additional References

[MenuMeter](http://www.ragingmenace.com/software/menumeters/index.html)
[MenuMeter El Capitan](https://github.com/yujitach/MenuMeters)
