# Welcome
My personal website is written using [Jekyll](https://jekyllrb.com) and hosted on [GitHub Pages](https://pages.github.com/).

I use the default minima theme, which I have modified a little bit to suit my needs:

* Multiple blog setup
* Angel.co social button
* Some smart filtering/routing using [Liquid](https://help.shopify.com/themes/liquid/basics)
* More tiny tweaks

## Running Locally
1. Install Ruby and [bundler](http://bundler.io/).
2. Clone this repo to a local directory.
3. `cd` to the directory and run `bundle install`.
4. To run locally, run `bundle exec jekyll serve`. I add the `--draft` flag to preview posts in my (non public) `_drafts` folder.
5. `jekyll serve` will return an IP. Paste this IP into your browser to see what your site will look like.

## Deploying to GitHub Pages
Create a new repo on your GitHub called `(your username).github.io` and commit the site files to it. The page will automatically be built and display at the URL.

## License

The following directories and their contents are Copyright Michael Switzer. You may not reuse anything therein without my permission:

* _posts/
* assets/

All other directories and files are MIT Licensed.