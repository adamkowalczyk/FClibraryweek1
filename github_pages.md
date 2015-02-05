# Github pages

### Gemfile

To make your local environment match github pages, create a Gemfile in your root (see docs below). This way we won't be caught out by version differences in jekyll's various dependancies.

Run "bundle install" initially, and "bundle update" in the future to stay up to date.

When serving your website locally, use "bundle exec jekyll serve" to run the jekyll serve command in the context of your bundle.

### Misc

You don't need to build your site if you don't want to, github pages will serve it from unbuilt jekyll. 

## Reference:

http://jekyllrb.com/docs/github-pages/

https://help.github.com/articles/using-jekyll-with-pages/