---
layout: post
title: The Ruby Programming Language
---
## Install Ruby
### Install [rbenv](https://github.com/rbenv/rbenv)

```shell
git clone https://github.com/rbenv/rbenv.git ~/.rbenv
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.zshrc
~/.rbenv/bin/rbenv init
type rbenv
# => "rbenv is a function"
```

### Install [ruby-build](https://github.com/rbenv/ruby-build)

```shell
git clone https://github.com/rbenv/ruby-build.git ~/.rbenv/plugins/ruby-build
```

### Install [ruby-gemset](https://github.com/jf/rbenv-gemset)

```shell
git clone git://github.com/jf/rbenv-gemset.git $HOME/.rbenv/plugins/rbenv-gemset
```

### Install Ruby

```shell
rbenv install 2.4.1
# env RUBY_BUILD_MIRROR_URL=file:///home/chironz/Downloads/ruby-2.4.1.tar.bz2# rbenv install 2.4.1
rbenv global 2.4.1
rbenv gemset create jekyll
mkdir project
cd project
rbenv gemset init jekyll
gem install bundler
```

### [Gem Source](https://gems.ruby-china.org/)

```shell
gem sources --add https://gems.ruby-china.org/ --remove https://rubygems.org/
bundle config mirror.https://rubygems.org https://gems.ruby-china.org
```

## Learn Ruby
