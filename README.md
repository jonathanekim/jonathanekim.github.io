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
bundle update --all
```

### Running Local Instance

```bash
bundle exec jekyll serve
```

Then open your browser to `http://localhost:4000`.

### Building for Google

```bash
bundle exec jekyll build --config _config.yml,_config_google.yml
```

## Site Structure

Originally based on the [Minima theme](https://jekyll.github.io/minima/) (Jekyll default), but heavily modified.

### Includes

Code snippets in `_includes` can be used in layouts or other includes.

* `disqus_comments.html`. Disqus comment box (active only in production).
* `footer.html`. Site `<footer>` section.
* `google-analytics.html`. Google Analytics (active only in production).
* `head.html`. Site `<head>` section.
* `header.html`. Site `<header>` section.
* `icon-* files`. Various icons.
* `intro.html`. Intro blurb.
* `portfolio-card.html`. Portfolio card section.

### Layouts

HTML files in `_layouts` use `_includes` to define a full page.

* `default.html`. Base layout.
* `home.html`. Home page layout.
* `page.html`. Generic page layout.
* `portfolio.html`. Portfolio item layout.
* `portfolios.html`. Portfolio collection layout.
* `post.html`. Blog post layout.
* `posts.html`. Blog post collection layout.

### Sass

Sass (`.scss`) files in `_sass` directory to style pages. These are processed into an `assets/main.css` file.

* `minima.scss`. Core style file imported by preprocessed `main.scss`. Defines theme variable defaults and imports sass partials.
* `minima/_base.scss`. Resets and defines base styles for various HTML elements.
* `minima/_includes.scss`. Defines styles for `_includes`.
* `minima/_layout.scss`. Defines styles for `_layouts`.
* `minima/_syntax-highlighting.scss`. Defines styles for syntax highlighting.

### Assets

`main.scss` and icons in `assets` used by the site. The directory is copied as is to the final site.

### Collections

* `_portfolio`. Contains portfolio items.
* `_posts`. Contains blog posts.
* `_site`. Static site generated by Jekyll. Do not modify directly.

## Customization

### Change default date format

Default date format can be changed by specifying `site.minima.date_format`
in `_config.yml`.

```yaml
# Minima date format
# refer to http://shopify.github.io/liquid/filters/date/ if you want to customize this
minima:
  date_format: "%b %-d, %Y"
```

--

### Enable Disqus comments

Enable comments by adding in `_config.yml`:

```yaml
  disqus:
    shortname: my_disqus_shortname
```

More about Disqus' shortnames: [here](https://help.disqus.com/customer/portal/articles/466208).

Comments can be disabled on a particular post by adding `comments: false` to that post's YAML Front Matter.
