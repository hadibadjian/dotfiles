# Hadi's dotfiles

Forked [Mathias Bynens'](https://github.com/mathiasbynens/dotfiles).

![prompt screen shot](https://igcdn-photos-h-a.akamaihd.net/hphotos-ak-xaf1/t51.2885-15/e35/c71.0.307.307/11821719_1607065079554863_1490092418_n.jpg)

## Additional Configurations

### Homebrew
`ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

### RVM
`curl -sSL https://get.rvm.io | bash -s stable --ruby`

Add the following to `~/.bash_profile`
```
# RVM
source ~/.rvm/scripts/rvm
```

### Sublime Packages

Package Manager
```
import urllib.request,os,hashlib; h = 'eb2297e1a458f27d836c04bb0cbaf282' + 'd0e7a3098092775ccb37ca9d6b2e4b7d'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

Useful Packages:
`Alignment, All Autocomplete, ApplySyntax, BracketHighlighter, Case Conversion, Cucumber, Gherkin (Cucumber) Formatter, GitGutter, MarkdownEditing, MarkdownTOC, Pretty JSON, RSpec, Theme - Spacegray`

MarkdownEditing User Settings
[Markdown.sublime-settings](init/Markdown.sublime-settings)

### Xcode

[Source Code Rro Font](https://github.com/adobe-fonts/source-code-pro)

[SpaceGray Theme](https://github.com/zdne/spacegray-xcode)

[Documenter](https://github.com/onevcat/VVDocumenter-Xcode)

### MenuMeter

[MenuMeter](http://www.ragingmenace.com/software/menumeters/index.html)
