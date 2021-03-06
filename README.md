dots
====

A new age reincarnation of my dotfiles, fucking clean, made with love.

P.S.: This is *my dotfiles*, there is my name & contacts everywhere. Don't
blindly use my settings as is.

installation
====

install [homebrew](http://brew.sh/):
```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

```
git clone http://github.com/vyorkin/dots ~/.dots
cd ~/.dots
git submodule update --init
make
```

syntastic eslint won't work until you install
[eslint_d](https://github.com/mantoni/eslint_d.js)

in case of problems with [tern_for_vim](https://github.com/ternjs/tern_for_vim):
```
cd $HOME/.vim/plugged/tern_for_vim
npm install
```

update ruby-build

```
cd ~/.rbenv/plugins/ruby-build && git pull origin master
```

# dont't forget

the fucking names:

* [brew bundler](https://github.com/Homebrew/homebrew-bundle)
* [showy edge](https://github.com/tekezo/ShowyEdge)
* [seil](https://pqrs.org/osx/karabiner/seil.html.en)
* [karabiner](https://pqrs.org/osx/karabiner/index.html.en)
* [Ilya Birman typography](http://ilyabirman.ru/projects/typography-layout/)
* [gitsome](https://github.com/donnemartin/gitsome)
* [z](https://github.com/rupa/z)
* [helium](http://heliumfloats.com/)
* [gg](https://github.com/qw3rtman/gg)
* [rainbowstream](https://github.com/DTVD/rainbowstream)

cvim chrome extension:
* [white theme](https://gist.github.com/vyorkin/711589d7f1a90954dec5)
* [cvimrc](https://gist.github.com/vyorkin/aa5abd74984fc77a17e5)
* [surfingkeys](https://gist.github.com/vyorkin/c5d9cfa63da9811ed0062c5f1440f754)

* [cheat](https://github.com/chrisallenlane/cheat)
* [tlrd](https://github.com/tldr-pages/tldr)

# resources
* [keyboard](https://github.com/jasonrudolph/keyboard)
* [rcm](http://thoughtbot.github.io/rcm/rcm.7.html)
* [awesome dotfiles](https://github.com/webpro/awesome-dotfiles)
* [how to setup tern](http://ternjs.net/doc/manual.html#configuration)
* [fasd](https://github.com/clvv/fasd#examples)

NeoVim terminfo fix for OSX:

https://github.com/neovim/neovim/issues/2048#issuecomment-78045837
```
infocmp $TERM | sed 's/kbs=^[hH]/kbs=\\177/' > $TERM.ti
tic $TERM.ti
```

How to install Emacs + Spacemacs:
```
brew install emacs --HEAD --use-git-head --with-cocoa --with-gnutls --with-rsvg --with-imagemagick
git clone https://github.com/syl20bnr/spacemacs ~/.emacs.d
```

Don't forget to create the `.ercpass` file in your home dir:

```
(setq freenode-password "your-password-goes-here")
(setq freenode-nick "your-password-goes-here")
(setq freenode-full-name "your-password-goes-here")
```

To suppress environment variable warnings put the following line in your `dotspacemacs/user-init`:
```
(setq exec-path-from-shell-arguments '("-l"))
```

To run local eslint npm module and fallback to global I use [this tiny vim plugin](https://github.com/mtscout6/syntastic-local-eslint.vim).

install a new node version & migrate existing packages:
```
nvm install new-version --reinstall-packages-from=old-version
```

install vagrant vmware plugin (if you have a license):

```
vagrant plugin install vagrant-vmware-fusion
vagrant plugin license vagrant-vmware-fusion license.lic
```

install gitsome:

```
sudo -H pip3 install gitsome
````

haskell tags:
[hasktags](https://hackage.haskell.org/package/hasktags) +
[haskdogs](https://github.com/grwlf/haskdogs)

Mac OS X Sierra & OpenSSH: [OpenSSH updates in macOS 10.12.2](https://developer.apple.com/library/content/technotes/tn2449/_index.html#//apple_ref/doc/uid/DTS40017589)

ocaml:

* install ocaml & opam
* `opam init`
* `opam install merlin`

[merlin + vim
setup instruction](https://github.com/ocaml/merlin/wiki/vim-from-scratch)

# troubleshooting

in case aflred can't find cask symlinks:
[go to alfred settings and just click on the 'reset'
button](https://github.com/caskroom/homebrew-cask/issues/9685#issuecomment-77553432)

macvim + python:
```
brew rm -f python
brew rm -f macvim
brew install python
brew linkapps python
brew install macvim --with-python --override-system-vim
brew linkapps macvim
```
