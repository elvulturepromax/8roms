# jekyll-theme-8bit

[![Build Status](https://travis-ci.org/julianolf/jekyll-theme-8bit.svg?branch=master)](https://travis-ci.org/julianolf/jekyll-theme-8bit) [![Gem Version](https://badge.fury.io/rb/jekyll-theme-8bit.svg)](https://badge.fury.io/rb/jekyll-theme-8bit)

A Jekyll theme inspired by classic 8bit games.

## Preview

You can see how the theme looks like [here](http://julianofernandes.com.br/jekyll-theme-8bit/).

## Installation

Add this line to your Jekyll site's `Gemfile`:

```ruby
gem "jekyll-theme-8bit"
```

And add this line to your Jekyll site's `_config.yml`:

```yaml
theme: jekyll-theme-8bit
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install jekyll-theme-8bit

## Contents

**jekyll-theme-8bit** has been scaffolded by the `jekyll new-theme` command and therefore has all the necessary files and directories to have a new Jekyll site up and running with zero-configuration.

### Layouts

Refers to files within the `_layouts` directory, that define the markup for your theme.

- `default.html` &mdash; The base layout that lays the foundation for subsequent layouts. The derived layouts inject their contents into this file at the line that says `{{ content }}` and are linked to this file via [FrontMatter](https://jekyllrb.com/docs/frontmatter/) declaration `layout: default`.
- `post.html` &mdash; The layout for your posts.

### Includes

Refers to snippets of code within the `_includes` directory that can be inserted in multiple layouts (and another include-file as well) within the same theme-gem.

- `downloads.html` &mdash; Insert download buttons when using the theme on a project with GitHub Pages enabled and the `show_downloads` variable set to *true* in `_config.yml`.
- `footer.html` &mdash; Defines the site's footer section.
- `fork-me.html` &mdash; Shows a *"Fork me on GitHub"* link when using the theme on a project with GitHub Pages enabled.
- `google-analytics.html` &mdash; Inserts Google Analytics module (active only in production environment).
- `head.html` &mdash; Code-block that defines the `<head></head>` in  _default_ layout.
- `header.html` &mdash; Defines the site's main header section. By default, pages with a defined `title` attribute will have links displayed here.
- `social.html` &mdash; Icons for social networks. Wich icons will be visible depends on what was defined in `_config.yml`.

### SASS

Refers to `.scss` files within the `_sass` directory that define the theme's styles.

- `fonts.scss` &mdash; Defines font faces used by 8bit's theme.
- `jekyll-theme-8bit.scss` &mdash; The core file imported by preprocessed `assets/css/style.scss`, it defines the defaults for the theme, layout, etc, and also further imports sass partials to supplement itself.
- `rouge-github.scss` &mdash; Defines the styles for syntax-highlighting.

### Assets

Refers to various asset files within the `assets` directory.

- `css/style.scss` &mdash; Imports sass files from within the `_sass` directory. It is what gets processed into the theme's main stylesheet `main.css` called by `_layouts/default.html` via `_includes/head.html`.
- `fonts/Press-Start-2P/` &mdash; The directory contains font files for *ttf*, *woff* and *woff2* formats.
- `js/scale-fix.js` &mdash; Zooming scale fix for iPhone.

This directory can include sub-directories to manage assets of similar type (`img`, `fonts`, `svg`), and will be copied over as is, to the final transformed site directory.

### Plugins

**jekyll-theme-8bit** comes with two plugins preinstalled.

- [`jekyll-paginate`](https://jekyllrb.com/docs/pagination/) &mdash; Allows break the main listing of posts up into smaller lists and display them over multiple pages. See [documentation](https://jekyllrb.com/docs/pagination/) for more details.
- [`jekyll-seo-tag`](https://github.com/jekyll/jekyll-seo-tag) &mdash; Ensure your website gets the most useful meta tags. See [usage](https://github.com/jekyll/jekyll-seo-tag/blob/master/docs/usage.md) to know how to set it up.

## Usage

TODO: Write usage instructions here. Describe your available layouts, includes, sass and/or assets.

## Contributing

Bug reports and pull requests are welcome. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## Development

To set up your environment to develop this theme, run `bundle install`.

Your theme is setup just like a normal Jekyll site! To test your theme, run `bundle exec jekyll serve` and open your browser at `http://localhost:4000`. This starts a Jekyll server using your theme. Add pages, documents, data, etc. like normal to test your theme's contents. As you make modifications to your theme and to your content, your site will regenerate and you should see the changes in the browser after a refresh, just like normal.

When your theme is released, only the files in `_layouts`, `_includes`, `_sass` and `assets` tracked with Git will be bundled.
To add a custom directory to your theme-gem, please edit the regexp in `jekyll-theme-8bit.gemspec` accordingly.

## License

The theme is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

## Credits

- 8bit style by [NES.css](https://nostalgic-css.github.io/NES.css/)
