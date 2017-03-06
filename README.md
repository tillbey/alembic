#alembic
# [Alembic](https://alembic.darn.es/)
[![Gem Version](https://badge.fury.io/rb/alembic-jekyll-theme.svg)](https://badge.fury.io/rb/alembic-jekyll-theme)

⚗ A Jekyll boilerplate theme designed to be a starting point for any Jekyll website.

![Screenshot](https://raw.githubusercontent.com/daviddarnes/alembic/master/screenshot.png)

## Contents
- [About](#about)
- [Features](#features)
- [Examples](#examples)
- [Installation](#installation)
- [Configuration](#configuration)
  - [Gem dependency settings](#gem-dependency-settings)
  - [Site settings](#site-settings)
  - [Site navigation](#site-navigation)
- [Using includes](#using-includes)
- [Page layouts](#page-layouts)
- [Page and Post options](#page-and-post-options)
- [Credits](#credits)

## About

Alembic is a starting point for [Jekyll](https://jekyllrb.com/) projects. Rather than starting from scratch, this boilerplate is designed to get the ball rolling immediately. Install it, configure it, tweak it, push it.

## Features

- Available as a starter kit or as [Jekyll 3.3 theme gem](http://jekyllrb.com/docs/themes/)
- Tested in all major browsers, that includes IE as well as Edge
- Extensive set of shortcodes to include various elements; such as buttons, icons, figure images and more
- Solid typographic framework from [Sassline](https://sassline.com/)
- Configurable navigation via a single file
- Modular Jekyll components
- Easily interchangeable sidebar
- Post category support in the form of a single post index page grouped by category
- Built in live search using JavaScript
- Contact form built in using [Formspree](https://formspree.io/)
- Works on [GitHub Pages](https://pages.github.com/) out of the box
- Built with [Jekyll](https://jekyllrb.com/) 3.3
- Designed with [Siteleaf](http://www.siteleaf.com/) in mind
- Has 9 of the most popular networks as performant sharing buttons
- Has documentation

## Examples

Here are a few examples of Alembic out in the wild being used in a variety of ways:

- [bitpodcast.com](https://bitpodcast.com/)
- [katiesimonemusic.com](http://katiesimonemusic.com/)
- [joelcagedesign.com](https://joelcagedesign.com/)
- [bawejakunal.github.io](https://bawejakunal.github.io/)
- [case2111.github.io](http://case2111.github.io/)
- [www.10people.co.uk](http://www.10people.co.uk/)

## Installation

### As a Boilerplate / Fork

1. [Fork the repo](https://github.com/daviddarnes/alembic#fork-destination-box)
2. Clone down the repo with `$ git clone git@github.com:username/reponame.git`
3. Delete the `demo/` folder and `screenshot.png` files
4. Change the `CNAME` record to your projects' record
5. Install bundler with `$ gem install bundler`
6. Install gems with `$ bundle install`
7. Run Jekyll with `$ bundle exec jekyll serve --watch`
8. Begin hacking for your project

### As a Jekyll 3.3 theme gem

1. Download the starter `/demo` content, [quick download link](https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/daviddarnes/alembic/tree/master/demo)
2. Install bundler with `$ gem install bundler`
3. Install gems with `$ bundle install`
4. Run Jekyll with `$ bundle exec jekyll serve --watch`
5. Begin hacking for your project

### Boilerplate & Theme differences

The boilerplate kit is better for more drastic hacking and changes, a project that's quite different to any other and needs a lot of custom work done. Additionally you'll only be able to use this method if you want to host it on GitHub Pages, as [themes can't be submitted](https://pages.github.com/themes/)... yet.

Using the theme will allow you to receive updates made and will be more programmatic. To make your own changes you'll need to overwrite the files with your own. For example: If I want to change the colours of my site I'll need to copy the [`_colors.scss`](https://github.com/daviddarnes/alembic/blob/master/_sass/_colors.scss) file and create my own in `_sass/colors.scss` with my own changes. This is the same for all files within the theme, which means your own project will be more lean than if you were to use the boilerplate.

## Configuration

There's a number of settings you'll need to change before you can start hacking away at files. Here's a run down of what you'll need to change:

### Gem dependency settings
`twitter`, `author` and `social` values will need to be changed to the projects' social information or removed. Look for the `Gem settings` comment within the `/_config.yml` file. These values are for the [jekyll-seo-tag](https://github.com/jekyll/jekyll-seo-tag) - follow the link to find out more.

### Site settings
You'll need to change the `description`, `title` and `url` to match with the project. You'll also need to replace the `/assets/placeholder-logo.svg` `/assets/placeholder-social.png` with project logo and default social image. The `email` needs to be changed to the email you want to receive contact form enquires with. The `disqus` value should be changed to your project username on [Disqus](https://disqus.com). Look for the `Site settings` comment within the `/_config.yml` file. The `repo` setting is optional, for now, and can be removed entirely, if you wish.

### Site navigation
There are 3 different navigation types: one for the header, one for the footer and one for a set of social links shown in the aside (or sidebar). If the header or footer navigation are removed, they will fallback to a list of pages within the site. The `social_navigation` properties should either be one that is already in the list (so `Twitter` or `Facebook`) or simply `link`, This is so an icon can be set for the link. Look for the `Site navigation` comment within the `/_config.yml` file.

## Using includes

There are 2 main types of includes: ones designed for the site and ones that are designed as shortcodes. Here are a list of the shortcode includes:

### `button.html`
A button that can link to a page of any kind.

Example usage: `{% include button.html text="I'm a button" link="https://daviddarnes.com" %}`

Available options:
- `text`: The text of the button _required_
- `link`: The link that the button goes to _required_
- `icon`: The icon that is added to the end of the button text
- `color`: The color of the button

### `figure.html`
An image with optional caption.

Example usage: `{% include figure.html image="/uploads/feature-image.jpg" caption="Check out my photo" %}`

Available options:
- `image`: The image shown _required_
- `caption`: A caption to explain the image
- `position`: The position of the image. `left`, `right` or `full`

### `icon.html`
An icon.

Example usage: `{% include icon.html id="twitter" %}`

Available options:
- `id`: The reference for the icon _required_
- `title`: The accessible label for the icon
- `color`: The desired colour of the icon

### `nav-share.html`
A set of buttons that share the current page to various social networks, which is controlled within the `_config.yml` file under the `sharing_links` keyword.

Example usage: `{% include nav-share.html %}`

Available options:
``` yml
Twitter: "#1DA1F2"
facebook: "#3B5998"
Google+: "#DC4E41"
Pinterest: "#BD081C"
LinkedIn: "#0077B5"
tumblr: "#36465D"
Reddit: "#FF4500"
Hacker News: "#ff6600"
Designer News: "#2D72D9"
Email: ""
```

_The first item is the name of the network (must be one of the ones stated above) and the second is the colour of the button. To remove a button just remove the line of the same name._

### `video.html`
A YouTube video.

Example usage: `{% include video.html id="zrkcGL5H3MU" %}`

Available options:
- `id`: The YouTube ID for the video _required_

### `map.html`
A Google map. _See Google [My Maps](https://www.google.com/mymaps)_

Example usage: `{% include map.html id="1UT-2Z-Vg_MG_TrS5X2p8SthsJhc" %}`

Available options:
- `id`: The map ID for the video _required_

### `site-form.html`
Adds a contact form to the page.

Example usage: `{% include site-form.html %}`

This include has no options. Use the `email` option in the `/_config.yml` to change to the desired email.

### `site-search.html`
Adds a search form to the page.

Example usage: `{% include site-search.html %}`

This include has no options. This include will add a block of javascript to the page and javascript reference in order for the search field to work correctly.

## Page layouts

As well as `page`, `post`, `blog`, there are a few alternative layouts that can be used on pages:

- `page-aside-left`: Places the aside (sidebar) to the left of the content
- `home`: Removes the aside entirely, leaving the full width for the main content (typically used for home page designs)
- `categories`: Shows all posts grouped by category, with an index of categories in a left hand sidebar
- `search`: Adds a search field to the page as well as a simplified version of the sidebar to allow more focus on the search results

## Page and Post options

There are some more specific options you can apply when creating a page or a post:

- `comments: false`: Turns off comments for that post
- `feature_image: "/uploads/feature-image.jpg"`: Adds a full width feature image at the top of the page
- `feature_text: "Example text"`: Adds text to the top of the page as a full width feature with solid colour; supports markdown. This can be used in conjunction with the `feature_image` option to create a feature image with text over it
- `indexing: false`: Adds a `noindex` meta element to the `<head>` to stop crawler bots from indexing the page, used on the 404 page

> **Note:** The Post List Page options are actually in the collection data within the `_config.yml` file.

## Credits

- Thanks to [Simple Icons](https://simpleicons.org/) for providing the brand icons, by [Dan Leech](https://twitter.com/bathtype)
- Thanks to [Sassline](https://sassline.com/) for the typographic basis, by [Jake Giltsoff](https://twitter.com/jakegiltsoff)
- Thanks to [Flexbox mixin](https://github.com/mastastealth/sass-flex-mixin) by [Brian Franco](https://twitter.com/brianfranco)
- Thanks to [Normalize](https://necolas.github.io/normalize.css/) by [Nicolas Gallagher](https://twitter.com/necolas) and [Jonathan Neal](https://twitter.com/jon_neal).
- Thanks to [pygments-css](http://richleland.github.io/pygments-css/) for the autumn syntax highlighting, by [Rich Leland](https://twitter.com/richleland)

#neo-hpstr-jekyll-theme
# [Neo-HPSTR Jekyll Theme](http://aronbordin.com/neo-hpstr-jekyll-theme)
[![Gem Version](https://badge.fury.io/rb/neo-hpstr-jekyll-theme.svg)](https://badge.fury.io/rb/neo-hpstr-jekyll-theme)

Neo-HPSTR Jekyll is a responsive and modern blog template.

![Preview](http://aron-bordin.github.io/neo-hpstr-jekyll-theme/images/neo-hpstr-jekyll-theme-preview.png)

Demo: http://aronbordin.com/neo-hpstr-jekyll-theme


## Contents

- [Installation](#installation)
- [Features](#features)
- [Configuration](#configuration)
- [Questions](#questions)
- [Contributing](#contributing)
- [Development](#development)
- [License](#license)

## Installation

### As a Boilerplate / Fork

1. [Fork the repo](https://github.com/aron-bordin/neo-hpstr-jekyll-theme)
2. Clone down the repo with `$ git clone git@github.com:username/reponame.git`
3. Delete the `demo/` folder and `screenshot.png` files
4. Install bundler with `$ gem install bundler`
5. Install gems with `$ bundle install`
6. Run Jekyll with `$ bundle exec jekyll serve --watch`
7. Begin hacking for your project

(If you are serving your blog at github, make sure to enale the gh-pages at yout repo settings)

### As a Jekyll >= 3.3 theme gem

If you already have a jekyll project, jump to the instructions bellow. Otherwise, follow these steps:

1. Install jekyll and bundler with `$ gem install jekyll bundler`.
2. Create your website `jekyll new my-awesome-blog`.
3. `cd my-awesome-blog`

Inside the project folder, install the theme as follows:

1. Download the starter `/demo` content, [quick download link](https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/aron-bordin/neo-hpstr-jekyll-theme/tree/master/demo) and extract the content to the blog folter.
2. Install bundler with `$ gem install bundler`
3. Install gems with `$ bundle install`
4. Run Jekyll with `$ bundle exec jekyll serve --watch`
5. Begin hacking for your project


### Boilerplate & Theme differences

The boilerplate kit is better for more drastic hacking and changes, a project that's quite different to any other and needs a lot of custom work done. Additionally you'll only be able to use this method if you want to host it on GitHub Pages, as [themes can't be submitted](https://pages.github.com/themes/)... yet.

Using the theme will allow you to receive updates made and will be more programmatic. To make your own changes you'll need to overwrite the files with your own.

## Features

* Modern design.
* Responsive templates for post, page, and home `_layouts`. Looks great on mobile, tablet, and desktop devices.
* Gracefully degrades in older browsers. Compatible with Internet Explorer 8+ and all modern browsers.
* Sweet topbar animated menu with support for drop-downs.
* Optional [Disqus](http://disqus.com) comments and social sharing links.
* [Open Graph](https://developers.facebook.com/docs/opengraph/) and [Twitter Cards](https://dev.twitter.com/docs/cards) support for a better social sharing experience.
* Simple [custom 404 page](x) to get you started.
* [Syntax highlighting](x) to make your code examples look snazzy
* Author panel, with social links

## Configuration

Here are some tips on how to customize your blog theme. If you have questions, just open a new issue :)

### Project tree

    ├── about.md                    # about page, /about/
    ├── assets/                     # css, js, fonts, etc
    ├── categories.html
    ├── _config.yml                 # your blog configuration
    ├── demo/                       # folder with quick start content
    ├── feed.xml                    # rss feed generator
    ├── Gemfile                     # project dependencies
    ├── Gruntfile.js                # some grunt tasks, useful for theme developing
    ├── images/                     # blog images
    ├── _includes
    │   ├── author.html             # author banner (at the end of post)
    │   ├── browser-upgrade.html    # ask for update
    │   ├── disqus_comments.html    # comments
    │   ├── feed-footer.html        # feed footers
    │   ├── footer.html             # page footer
    │   ├── gallery                 # used for displaying images in a page
    │   ├── header.html             # header menu
    │   ├── head.html               # site head, with css includes and metadata
    │   ├── icons.html              # site icons
    │   ├── pagination.html         # pagination
    │   ├── read-more.html          # read-more banner, to recommend posts
    │   ├── scripts.html            # js scripts
    │   └── social-share.html       # floating social share integration
    ├── index.html                  # homepage
    ├── _layouts                    # blog layouts
    │   ├── dark-post.html
    │   ├── home.html
    │   ├── page.html
    │   └── post.html
    ├── LICENSE.txt
    ├── neo-hpstr-jekyll-theme.gemspec
    ├── package.json
    ├── _posts                     # sample posts
    │   ├── 2016-11-26-sample-post-images.md
    │   ├── 2016-11-27-video-post.md
    │   ├── 2016-11-28-sample-link-post.md
    │   ├── 2016-11-29-background-image.md
    │   ├── 2016-11-30-dark-post.md
    │   ├── 2016-12-01-code-highlighting-post.md
    │   └── 2016-12-02-sample-post.md
    ├── posts.html                 # page for listing posts
    ├── README.md
    ├── _sass                      # blog style
    ├── screenshoot.png
    ├── search.html                # search page
    ├── search.json
    ├── _site/
    ├── tags.html                  # tags page


### Disqus Comments

Create a [Disqus](http://disqus.com) account and change `disqus_shortname` in `_config.yml` to the Disqus *shortname* you just setup. By default comments appear on all post and pages if you assigned a shortname. To disable commenting on a post or page, add the following to its YAML Front Matter:

    comments: false

### Social Share Links

To disable Facebook, Twitter, and Google+ share links on a post or page, add the following to its front matter:

    share: false

### Floating Social Share Links

To enable floating share links on the left of the screen, edit it on `_config.yml`:

    float_share: true

### Owner/Author Information

Change your name, and avatar photo (200x200 pixels or larger), email, and social networking URLs. If you want to link to an external image on Gravatar or something similar you'll need to edit the path in `_includes/author.html` since it assumes it is hosted on your site.

### Google Analytics and Webmaster Tools

Your Google Analytics ID goes here along with meta tags for [Google Webmaster Tools](http://support.google.com/webmasters/bin/answer.py?hl=en&answer=35179) and [Bing Webmaster Tools](https://ssl.bing.com/webmaster/configure/verify/ownershi) site verification.

### Top Menu - Navigation Links

To add additional links in the menu edit `_config.yml`. Use the following format to set the URL and title for as many links as you'd like. *External links will open in a new window..* You can create a sub-category using the `submenu` item. Also, you can list your post categories setting the `type: 'categories'`


    menu:
      - title: 'Home'
        url: '/'
      - title: 'Fork'
        url: 'http://github.com/aron-bordin/neo-hpstr-jekyll-theme'
      - title: 'Tags'
        url: '/tags'
      - title: 'Categories'
        url: '/categories'
        type: 'categories'
      - title: 'Favorites'
        url: '#'
        submenu:
          - title: 'highlighter'
            url: '/code-highlighting-post/'
          - title: 'intro'
            url: '/sample-post/'

### Adding New Content with Octopress

While completely optional, I've included Octopress and some starter templates to automate the creation of new posts and pages. To take advantage of it start by installing the [Octopress](https://github.com/octopress/octopress) gem if it isn't already.

    $ gem install octopress

#### New Post

Default command

    $ octopress new post "Post Title"

Default works great if you want all your posts in one directory, but if you're like me and want to group them into subfolders like `/posts`, `/portfolio`, etc. Then this is the command for you. By specifying the DIR it will create a new post in that folder and populate the `categories:` YAML with the same value.

    $ octopress new post "New Portfolio Post Title" --dir portfolio

#### New Page

To create a new page use the following command.

    $ octopress new page new-page/

### Style Customization

Here you'll find some useful scss variables to help you to customize your Blog interface. All variables can be found at `_sass/_variables.scss`.

#### Top Navbar Size

To change its size, edit the **`$menu-height`** value. It's recommended a value between 50px and 100px. This variable will automatically update the icon and menu size for you.

#### Top Navbar Colors

The navbar uses two colors, the top color and overflow color. The top color represents the navbar color when the window is not scrolled and the overflow color represents the color when we have a sufficient scroll to change its color.

You can change these colors using the **`$menu-top`** and **`$menu-overflow`** variable values.

#### Top Navbar hover color

The color that you see in the item under the mouse can be changed in the **`$header-margin`** variable.

### Further Customization

Jekyll 2.x added support for Sass files making it much easier to modify a theme's fonts and colors. By editing values found in `_sass/variables.scss` you can fine tune the site's colors and typography.

For example if you wanted a red background instead of white you'd change `$bodycolor: #fff;` to `$bodycolor: $cc0033;`.

To modify the site's JavaScript files I setup a Grunt build script to lint/concatenate/minify all scripts into `scripts.min.js`. [Install Node.js](http://nodejs.org/), then [install Grunt](http://gruntjs.com/getting-started), and then finally install the dependencies for the theme contained in `package.json`:

    npm install

From the theme's root, use `grunt` to concatenate JavaScript files and optimize `.jpg`, `.png` and `.svg` files in the `images/` folder.

You can also use `grunt dev` in combination with `bundle exec jekyll serve` to watch for updates in JS files that Grunt will then automatically re-build as you write your code, which will in turn auto-generate your Jekyll site when developing locally.

## Questions?

Having a problem getting something to work or want to know why I setup something in a certain way?  [File a GitHub Issue](http://github.com/aron-bordin/neo-hpstr-jekyll-theme/issues/new). And if you make something cool with this theme feel free to let me know.

## Contributing


Bug reports and pull requests are welcome on GitHub at https://github.com/aron-bordin/neo-hpstr-jekyll-theme. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## Development

To set up your environment to develop this theme, run `bundle install`.

Your theme is setup just like a normal Jekyll site! To test your theme, run `bundle exec jekyll serve` and open your browser at `http://localhost:4000`. This starts a Jekyll server using your theme. Add pages, documents, data, etc. like normal to test your theme's contents. As you make modifications to your theme and to your content, your site will regenerate and you should see the changes in the browser after a refresh, just like normal.

When your theme is released, only the files in `_layouts`, `_includes`, and `_sass` tracked with Git will be released.

## License

The theme is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
