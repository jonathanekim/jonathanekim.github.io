# jonathankim.github.io

Personal site for Jonathan Kim. Built using Jekyll.

## Setup

```bash
git clone <repository>
brew install rbenv
rbenv init
curl -fsSL https://github.com/rbenv/rbenv-installer/raw/master/bin/rbenv-doctor | bash
rbenv install -l
rbenv install $(rbenv local)
which -a gem
gem install bundler
bundle install
```

## Running Local Instance

```bash
bundle exec jekyll serve
```
