# A minimalist Octopress theme with MathJax support

## Features

- MathJax scripts and CSS bugfix are already included in the theme templates
- Custom landing page instead of the blog as the default
- Simple default navigation

![Landing page screenshot](http://i.imgur.com/QprLjmK.png)

## Installation

### 1. Apply the theme

    $ cd octopress/
    $ git clone git@bitbucket.org:stchangg/mathy.git .themes/mathy
    $ rake install[mathy]

### 2. Use kramdown instead of rdiscount

[kramdown](http://kramdown.rubyforge.org/) is a fast, pure-Ruby Markdown-superset converter. Unlike rdiscount, it can properly process MathJax markup.

1. In `Gemfile`, replace the entire `gem 'rdiscount'` line (including the version part) with `gem 'kramdown'`.
2. Run `bundle install`.
3. In `_config.yml`, replace `markdown: rdiscount` with `markdown: kramdown`.

Source: http://blog.zhengdong.me/2012/12/19/latex-math-in-octopress

### 3. Customize these files before deploying

- Landing page: `source/index.markdown`
- "About" page: `source/about/index.markdown`

### 4. Optional further configuration

- Favicon: `source/favicon.png`
- Navigation: `source/_includes/custom/navigation.html`

#### Add an "about me" section to the sidebar

![About me section screenshot](http://i.imgur.com/lb2Szmt.png)

Edit `source/_includes/custom/asides/aboutme.html`

In `_config.yml`, add the "aboutme" module to the sidebar asides:

    default_asides: [custom/asides/aboutme.html, ...]
