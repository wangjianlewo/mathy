# A minimalist Octopress theme with MathJax support

## Features

- MathJax support is built in
- Custom landing page instead of the blog as the default
- Simple default navigation

## Installation

### 1. Apply the theme

    $ cd octopress/
    $ git clone git@bitbucket.org:stchangg/mathy.git .themes/mathy
    $ rake install[mathy]  # no quotes needed!

### 2. Use `kramdown` instead of `rdiscount` to parse math markup properly
Source: http://www.idryman.org/blog/2012/03/10/writing-math-equations-on-octopress/

1. Install `kramdown`

    gem install kramdown

2. Change `_config.yml`

    -markdown: rdiscount
    +markdown: kramdown

3. Change `Gemfile`

    -gem 'rdiscount', '~> 2.0.7'
    +gem: 'kramdown'

### 3. Edit these files before deploying

- Landing page: `source/index.markdown`
- "About" page: `source/about/index.markdown`

### 4. Optional further configuration

- Favicon: `source/favicon.png`
- Navigation: `source/_includes/custom/navigation.html`

#### Add an "about me" section to the sidebar

- Edit `source/_includes/custom/asides/aboutme.html`

In `_config.yml`, add the "aboutme" module to the sidebar asides:

    default_asides: [custom/asides/aboutme.html, ...]
