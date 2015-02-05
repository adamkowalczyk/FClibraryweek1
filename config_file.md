# Config file



The default jekyll config file looks like this:

```
# Site settings
title: Your awesome title
email: your-email@domain.com
description: > # this means to ignore newlines until "baseurl:"
  Write an awesome description for your new site here. You can edit this
  line in _config.yml. It will appear in your document head meta (for
  Google search results) and in your feed.xml site description.
baseurl: "" # the subpath of your site, e.g. /blog/
url: "http://yourdomain.com" # the base hostname & protocol for your site
twitter_username: jekyllrb
github_username:  jekyll

# Build settings
markdown: kramdown
```
As you can see some changes need to be made.

Be aware, if for some reason you are using a 'project page' rather than a 'personal page' you will need to set the baserul to "/my-project".

## Reference:

http://jekyllrb.com/docs/configuration/
