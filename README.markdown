# A minimalist Octopress theme with MathJax support

## Features

- MathJax support is built in
- Won't clobber your existing files when you re-install the theme

## Installation

This theme expects (and won't work without):

- A custom landing page at /
- An "About me" section in the sidebar
- An "About" page at /about

The following steps will walk you through the process of adding them.

### 1. Install the theme

    $ cd octopress/
    $ rake install[mathy]  # no quotes needed!

### 2. Create your landing page

    $ touch index.markdown

Suggested contents for `/index.markdown`:

    ---
    layout: page
    ---

    ## Welcome to my website!

    ### Fun links
    ...

    ### More stuff
    ...

### 3. Add the "About me" section to the sidebar

    $ touch source/_includes/custom/asides/aboutme.html

Suggested contents for `source/_includes/custom/asides/aboutme.html`:

    <section>
      <img style="height:250px;" src="images/your-image-here.png"/>
      <p>
        Your bio here.
      </p>
    </section>

### 4. Create your about page

    $ rake new_page[about]

Suggested contents for `/about/index.markdown`:

    ---
    layout: page
    ---

    ## About me
    ...

    ## Contact
    ...

## Caveats

I decided to not include the expected files in the theme because I wanted to tweak the theme and re-install it without clobbering the custom pages I had added to my site. As a result, initial set-up becomes slightly more difficult. :(

I might change my mind and favor the initial set-up case over the update case.

Ideally, there'd be some way in Octopress to completely isolate themes from user-generated content, or for Octopress to support a theme install mode that will skip copying over files that have already been defined by the user. Maybe I'll get around to submitting a pull request someday...
