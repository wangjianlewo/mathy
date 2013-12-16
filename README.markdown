# A minimalist Octopress theme with MathJax support

## Features

- MathJax support is built in
- Custom landing page instead of the blog as the default
- Simple default navigation

## Installing the theme for the first time

    $ cd octopress/
    $ git clone git@bitbucket.org:stchangg/mathy.git .themes/mathy
    $ rake install[mathy]  # no quotes needed!

## Things you'll want to edit before deploying

- Landing page: `source/index.markdown`
- "About" page: `source/about/index.markdown`

## Optional further configuration

- Favicon: `source/favicon.png`
- Navigation: `source/_includes/custom/navigation.html`

### "About me" section of sidebar

- Edit `source/_includes/custom/asides/aboutme.html`

In `_config.yml`, add the "aboutme" module to the sidebar asides:

    default_asides: [custom/asides/aboutme.html, ...]
