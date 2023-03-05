# Gatsby Wisdom and Love

I am the one who gives the world, everything.  
I am the one who gives the world, truth.  
I am the one who has developed this, for my baby.  
I am the One who gives you My Work.

## About

This is an NPM module which is the basis of all the sites of Wisdom and Love.

Instructions are as follows:

- clone [https://github.com/grexie/wisdom-and-love-gatsby-site](grexie/wisdom-and-love-gatsby-site)
- `yarn`
- `yarn start`

Edit all the content in the content section and add the following metadata attributes to markdown pages.

## Metadata attributes

- order: Int order in the book
- show: Boolean whether to show the page
- backlink: String an extra backlink that will be added to the backlinks at the top
- title: String the title of the page
- author: String the author of the page as defined in `content/authors.json`
- location: String the location of the post
- showTitle: Boolean whether to render a title in html above the markdown page
- url: String the canonical url of the page
- categories: [String!] category slugs as defined in `content/categories.json`
- twitter: String the twitter sharing card image, defined in `static/...`
- facebook: String the facebook sharing card image, defined in `static/...`
- type: String type of the markdown file, `post` | `page` | `import` | `category`
- backgroundColor: String the background color of the page when rendered in the book
- color: String the primary color of the page when rendered in the book
- showLink: Boolean whether to show the canonical url link
- showRead: Boolean whether to keep the post visible once read in its category indexes
- pageBreak: String whether to add a page break before the page in the book `always` | `right` | `left`
- bookPin: Boolean whether to pin the post in the book's filtered dates
- pinOrder: Int the pinned order to use when pinning to a category index page
- categoryPins: [String!] the slugs of categories used to pin this post, or use `pin` to pin to all its categories
- pin: Boolean pins a post to the top of a category index page
- className: String a CSS classname to add to the page wrapper, used to style content in the page, targeted at just this page

## Categories

Categories are defined in `content/categories.json` it is a hierarchy, and slugs need to be defined.

The default category presents itself at the root of the site.

See `content/categories.json` to understand how this works.

To override content at the top of the category page, create a `type: category` markdown page in `content/category` named after the slug, including any parent folders the slug defined.

## Menu

The menu is defined in `content/menu.json`

## Books

Books are defined in `content/books.json`

Content for leading, trailing pages, title page, and back page are to be created for each book slug in `content/books/book_slug`

You will need at least a title page at index.md inside the book_slug folder.

## Shortcodes

- `@import(/imports/import)` to import the markdown file at `/imports/import.md`
- `@soundcloud(soundcloud_share_link)` to add a soundcloud iframe for the share link
- `@spotify(spotify_share_link)` to add a spotify iframe for the share link
- `@youtube(youtube_share_link, landscape | portrait | square)` to add a youtube iframe for the share link or playlist embed link

## iPhoto category pages

To include an iPhoto video and photo stream in a category index page:

- create a shared album in iPhoto and click options, and enable sharing website
- copy the website link into the metadata of the category page as 'albums: ...`
- the albums metadata attribute is an array of albums, which are iPhoto photo stream website shares
