# Directory Structure

## Warning!

Never work on a file in **_site**.  
Jekyll rewrites this dir on every build.

##Structure:

Jekyll uses a standard directory structure to define your website. Resources need to put in particular places, and some aspects of your directory structure are translated directly into the finished site, e.g. file/directory names become URLS.

```
.
├── _config.yml
├── _drafts
|   ├── begin-with-the-crazy-ideas.textile
|   └── on-simplicity-in-technology.markdown
├── _includes
|   ├── footer.html
|   └── header.html
├── _layouts
|   ├── default.html
|   └── post.html
├── _posts
|   ├── 2007-10-29-why-every-programmer-should-play-nethack.textile
|   └── 2009-04-26-barcamp-boston-4-roundup.textile
├── _data
|   └── members.yml
├── _site
└── index.html
```

### What are they?

Each of these folders has a distinct purpose within Jekyll.

The _drafts folder is where you keep not-to-be-published posts. The advantage of having such a folder is that it allows you to locally preview a post by using the jekyll serve --drafts command.

The _includes folder is where you can keep blocks of code that you are likely to reuse a lot. This lets you keep your code dry and clean. If, for example, you have a certain header style that you wish to appear on most pages, and those pages use different layouts, rather than repeating yourself across layouts, you can simply specify {% include header %} to inject the header file within the _includes folder in each layout.

The _layouts folder is where much of the jekyll magic resides. This is where you specify templates in which your posts and pages will be wrapped in according to what they specify in their YAML Front Matter. In other words, this is where you specify presentation themes that your content can grab.

The _posts folder is where you stick your blog posts. These must follow the naming format of YYYY-MM-DD-title.markupextension and begin with YAML Front Matter. Other than that, you can simply type your blog post in the file and it will be processed by jekyll, fully formatted according to the layout specified in the Front Matter.

The _data folder is the content-parallel to the _includes folder. This is where you might store, for example, a memberlist.yml file, in which are a list of members whom you refer to frequently on different web pages. Rather than repeating yourself, you can simply reference the data file thusly: {% site.data.memberlist %}

### Getting started:

You too can have such a directory structure!

Once jekyll is installed, run "jekyll new ." (notice the full stop) in an empty directory (or "jekyll new dirname"), and the default jekyll site will appear.

## Reference:

http://jekyllrb.com/docs/structure/

http://pixelcog.com/blog/2013/jekyll-from-scratch-core-architecture/

http://destroytoday.com/blog/hello-world-im-jekyll/