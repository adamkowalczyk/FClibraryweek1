# Liquid

Liquid is a template engine with simple markup that apparently produces beautiful results.

There are two types of markup in liquid: output and tag.

### Output

Output uses the double curly brace syntax, e.g. 

```{{ page.title }}```

Using output tags you can access objects (variables) defined in your YAML front matter, or by Jekyll and out put them to your page.


You can also use simple methods in the form of filters. These have great usefulness. These take the form:
```{{ input | filter [| filter...] }}```


The following filter takes the title of a post, truncates it to ten words, then capitalizes it:
```{{ post.title | truncatewords: 10 | capitalize }}```

### Tags

Tags may not resolve to text, and take the form:

```{% comment %} this text wont be seen {% endcomment %}```

Tags are a bit more complicated. These are used for logical operations. One such operation is the for-loop:
```
{% for post in site.posts %}
<HTML STUFF>
{% endfor %}
```
An example of what this can do is found in the default jekyll template:
```
<ul>
  {% for post in site.posts reversed limit: 5 %}
    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>```

### Reference:

* Liquid Docs  
http://docs.shopify.com/themes/liquid-documentation/basics

* liquid for designers
https://github.com/Shopify/liquid/wiki/Liquid-for-Designers

