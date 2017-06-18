---
layout: post
title: Live In Spacemacs
---
#### System Information
* Hardware: MacBook Pro
* Software: macOS 10.12.4 (16E195)

#### Install GNU Emacs
* Install Homebrew

```sh
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
* Install GNU Emacs

```sh
brew install emacs --with-cocoa
```

#### InstalL Spacemacs

* Clone Spacemacs

```sh
git clone https://github.com/syl20bnr/spacemacs ~/.emacs.d
```

```sh
ls -aF |grep emacs
# =>
# .emacs.d/
```
* Launch Emacs
  * What is your preferred editing style? [vim/emacs]
  * What distribution of spacemacs would you like to start with?[standard/minimalist]
  * What type of completion framework do you want? [helm/ivy]

```sh
ls -aF |grep emacs
# =>
# .emacs.d/
# .spacemacs #
```

* Install [Source Code Pro](https://github.com/adobe-fonts/source-code-pro)
Launch Font Book App to install font 

#### Make dot directory are under source control

```sh
cd
mkdir .spacemacs.d
git init

mv .spacemacs .spacemacs.d/init.el
echo "# spacemacs-d" >> README.md

git add .
git commit -m "first commit"
git remote add origin git@github.com:chironz/spacemacs-d.git
git push -u origin master

ln -s ~/.spacemacs.d ~/Code/spacemacs-d
```

#### Spacemacs Configuration

```
(osx :variables osx-dictionary-dictionary-choice "English")
     helm
     auto-completion
     better-defaults
     emacs-lisp
     git
     markdown
     org
     (shell :variables
            shell-default-height 30
            shell-default-position 'bottom)
     spell-checking
     syntax-checking
     version-control
)

# Maximized At Startup
dotspacemacs-maximized-at-startup t
```

#### Spacemacs Shortcut

##### Window manipulation

| Key      | Description                            |
| :------- | :------------------------------------- |
| _ w v    | vertical split                         |
| _ w V    | vertical split and focus new window    |
| _ w s    | horizontal split                       |
| _ w s    | horizontal split                       |
| _ w d    | delete a window                        |



#### Use Spacemacs and Jekyll to write Blog 

* Install [Jekyll::Compose](https://github.com/jekyll/jekyll-compose)

```rb
gem 'jekyll-compose', group: [:jekyll_plugins]
```

* Jekyll::Compose Usage

```sh
draft      # Creates a new draft post with the given NAME
post       # Creates a new post with the given NAME
publish    # Moves a draft into the _posts directory and sets the date
unpublish  # Moves a post back into the _drafts directory
page       # Creates a new page with the given NAME
```
