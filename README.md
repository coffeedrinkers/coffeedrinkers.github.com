# Quick & Dirty Crash Course on CoffeeDrinkers.org Post Formatting

Back when Brotherhood of the Bean was up it used WordPress which was prone to bugs, and database driven.  Posts would be generated on the fly as needed.  As a result, sites using this model can be slow when heavily accessed, and because WordPress uses PHP, frequently hacked (usually via poor programming in a third party plugin).

So I decided to go a different route with coffeedrinkers.org.  I am a big fan of a text processing system called LaTex that can take text files with code markup and transform it into beautiful professional typeset documents.

Jekyll is a blog publishing platform that works off the same principle.  Posts are individual text files that contain markup, usually just a header.  Jekyll processes these files and spits out static HTML files.  Since there is nothing to process when a reader accesses these pages, they are very fast.  And since there are no moving parts, as long as access is controlled to github.com where the files are stored, the threat of hacking is very low.

As an author you have a few options. 

Option 1:  Write your post up in your favorite text editor.  Send it to me along with any image files you want included, and I'll do the heavy lifting.

Option 2:  Have a crack at formatting your post using the guidelines below.  Then send to me with any images.

For right now, I am going to restrict uploading of new posts to github.  Github is a code repository, as such when updates are made (commits) the previous version information is kept if a rollback is needed.  

# Post Formatting
Posts are text with markup.  All posts to coffeedrinkers.org must have the following header information.  Three types of posts are shown:

~~~ html
---
layout: post
title: ""
excerpt: ""
modified: 
categories: news
tags: [News]
image:
  feature: news-default.jpg
  credit: WeGraphics
  creditlink: http://wegraphics.net/downloads/free-ultimate-blurred-background-pack/
comments: true
share: true
author: 
---
![Aerobie AeroPress](/images/aeropress-hero-260.jpg){: .pull-right}

---
layout: post
title: ""
excerpt: ""
modified: 
categories: opinions
tags: [Opinion]
image:
  feature: opinions-default.jpg
  credit: WeGraphics
  creditlink: http://wegraphics.net/downloads/free-ultimate-blurred-background-pack/
comments: true
share: true
author: 
---
![Aerobie AeroPress](/images/aeropress-hero-260.jpg){: .pull-right}

---
layout: post
title: ""
excerpt: ""
modified: 
categories: reviews
tags: [Review]
image:
  feature: review-default.jpg
  credit: WeGraphics
  creditlink: http://wegraphics.net/downloads/free-ultimate-blurred-background-pack/
comments: true
share: true
author: 
---
![Aerobie AeroPress](/images/aeropress-hero-260.jpg){: .pull-right}
~~~

# Sample Post using the Template (Muchochecko):
~~~ html
---
layout: post
title: "This is a Review"
excerpt: "This Review is about coffee.  This excerpt will appear on under the title."
modified: (Leave Blank, this is for overrides)
categories: reviews  (One category per post, valid categories: reviews, opinions, news)
tags: [Review, Dan] 
image:
  feature: review-default.jpg
  credit: WeGraphics
  creditlink: http://wegraphics.net/downloads/free-ultimate-blurred-background-pack/
comments: true
share: true
author: muchochecko
---
![Name of Image you want to appear on the right](/images/image_name.jpg){: .pull-right}Hi this is my first post!
~~~

# Sample Post using the Template (Olaf):
~~~ html
---
layout: post
title: "This is a Review"
excerpt: "This Review is about coffee.  This excerpt will appear on under the title."
modified: (Leave Blank, this is for overrides)
categories: reviews  (One category per post, valid categories: reviews, opinions, news)
tags: [Review, Olaf] 
image:
  feature: review-default.jpg
  credit: WeGraphics
  creditlink: http://wegraphics.net/downloads/free-ultimate-blurred-background-pack/
comments: true
share: true
author: olaf
---
![Name of Image you want to appear on the right](/images/image_name.jpg){: .pull-right}Hi this is my first post!
~~~

# Sample Post using the Template (Mary):
~~~ html
---
layout: post
title: "This is a Review"
excerpt: "This Review is about coffee.  This excerpt will appear on under the title."
modified: (Leave Blank, this is for overrides)
categories: reviews  (One category per post, valid categories: reviews, opinions, news)
tags: [Review, Mary] 
image:
  feature: review-default.jpg
  credit: WeGraphics
  creditlink: http://wegraphics.net/downloads/free-ultimate-blurred-background-pack/
comments: true
share: true
author: mary
---
![Name of Image you want to appear on the right](/images/image_name.jpg){: .pull-right}Hi this is my first post!
~~~

# Post Text File Naming
All posts get named in the following manner:
**YYYY-MM-DD-Name-Of-The-Post.md**


## HTML Elements

Below is just about everything you'll need to style in the theme. Check the source code to see the many embedded elements within paragraphs.

# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6

~~~ html
# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6
~~~

### Body text

*This is emphasized*.

**This is bold.**

~~~ html
*This is emphasized*.
**This is bold.**
~~~

For Coffeedrinkers.org's Theme there are some special ways to diplay images:

Right/Left/Center Aligned Image, use this Code:
~~~ html
![Smithsonian Image]({{ site.url }}/images/3953273590_704e3899d5_m.jpg)
{: .image-pull-right}

Left Image
![Smithsonian Image]({{ site.url }}/images/3953273590_704e3899d5_m.jpg)
{: .image-pull-left}

Center Image
![Smithsonian Image]({{ site.url }}/images/3953273590_704e3899d5_m.jpg)
{: .image-pull-center}
~~~

### Blockquotes

> Lorem ipsum dolor sit amet, test link adipiscing elit. 
  
~~~ html
> Lorem ipsum dolor sit amet, test link adipiscing elit. 
~~~

## List Types

### Ordered Lists

1. Item one
   1. sub item one
   2. sub item two
   3. sub item three
2. Item two

### Unordered Lists

* Item one
* Item two
* Item three

## Tables

| Header1 | Header2 | Header3 |
|:--------|:-------:|--------:|
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|----
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|=====
| Foot1   | Foot2   | Foot3


~~~ html
### Ordered Lists

1. Item one
   1. sub item one
   2. sub item two
   3. sub item three
2. Item two

### Unordered Lists

* Item one
* Item two
* Item three

## Tables

| Header1 | Header2 | Header3 |
|:--------|:-------:|--------:|
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|----
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|=====
| Foot1   | Foot2   | Foot3

~~~

## Buttons

Make any link standout more when applying the `.btn` class.

~~~ html
<div markdown="0"><a href="#" class="btn">Primary Button</a></div>
<div markdown="0"><a href="#" class="btn btn-success">Success Button</a></div>
<div markdown="0"><a href="#" class="btn btn-warning">Warning Button</a></div>
<div markdown="0"><a href="#" class="btn btn-danger">Danger Button</a></div>
<div markdown="0"><a href="#" class="btn btn-info">Info Button</a></div>
~~~


## Notices

~~~ html
**Watch out!** You can also add notices by appending `{: .notice}` to a paragraph.
~~~


## Dealing with Images

Here are some examples of what a post with images might look like. If you want to display two or three images next to each other responsively use `figure` with the appropriate `class`. Each instance of `figure` is auto-numbered and displayed in the caption.

### Figures (for images or video)

#### One Up

<figure>
	<a href="http://farm9.staticflickr.com/8426/7758832526_cc8f681e48_b.jpg"><img src="http://farm9.staticflickr.com/8426/7758832526_cc8f681e48_c.jpg"></a>
	<figcaption><a href="http://www.flickr.com/photos/80901381@N04/7758832526/" title="Morning Fog Emerging From Trees by A Guy Taking Pictures, on Flickr">Morning Fog Emerging From Trees by A Guy Taking Pictures, on Flickr</a>.</figcaption>
</figure>

~~~ html
<figure>
	<a href="http://farm9.staticflickr.com/8426/7758832526_cc8f681e48_b.jpg"><img src="http://farm9.staticflickr.com/8426/7758832526_cc8f681e48_c.jpg"></a>
	<figcaption><a href="http://www.flickr.com/photos/80901381@N04/7758832526/" title="Morning Fog Emerging From Trees by A Guy Taking Pictures, on Flickr">Morning Fog Emerging From Trees by A Guy Taking Pictures, on Flickr</a>.</figcaption>
</figure>
~~~

#### Two Up

Apply the `half` class like so to display two images side by side that share the same caption.

~~~ html
<figure class="half">
    <a href="/images/image-filename-1-large.jpg"><img src="/images/image-filename-1.jpg"></a>
    <a href="/images/image-filename-2-large.jpg"><img src="/images/image-filename-2.jpg"></a>
    <figcaption>Caption describing these two images.</figcaption>
</figure>
~~~

And you'll get something that looks like this:

<figure class="half">
	<a href="http://placehold.it/1200x600.JPG"><img src="http://placehold.it/600x300.jpg"></a>
	<a href="http://placehold.it/1200x600.jpeg"><img src="http://placehold.it/600x300.jpg"></a>
	<figcaption>Two images.</figcaption>
</figure>

#### Three Up

Apply the `third` class like so to display three images side by side that share the same caption.

~~~ html
<figure class="third">
	<img src="/images/image-filename-1.jpg">
	<img src="/images/image-filename-2.jpg">
	<img src="/images/image-filename-3.jpg">
	<figcaption>Caption describing these three images.</figcaption>
</figure>
~~~

And you'll get something that looks like this:

<figure class="third">
	<img src="http://placehold.it/600x300.jpg">
	<img src="http://placehold.it/600x300.jpg">
	<img src="http://placehold.it/600x300.jpg">
	<figcaption>Three images.</figcaption>
</figure>

  

### Standard Code Block

    {% raw %}
    <nav class="pagination" role="navigation">
        {% if page.previous %}
            <a href="{{ site.url }}{{ page.previous.url }}" class="btn" title="{{ page.previous.title }}">Previous article</a>
        {% endif %}
        {% if page.next %}
            <a href="{{ site.url }}{{ page.next.url }}" class="btn" title="{{ page.next.title }}">Next article</a>
        {% endif %}
    </nav><!-- /.pagination -->
    {% endraw %}


### Fenced Code Blocks

~~~ css
#container {
    float: left;
    margin: 0 -240px 0 0;
    width: 100%;
}
~~~

~~~ html
{% raw %}<nav class="pagination" role="navigation">
    {% if page.previous %}
        <a href="{{ site.url }}{{ page.previous.url }}" class="btn" title="{{ page.previous.title }}">Previous article</a>
    {% endif %}
    {% if page.next %}
        <a href="{{ site.url }}{{ page.next.url }}" class="btn" title="{{ page.next.title }}">Next article</a>
    {% endif %}
</nav><!-- /.pagination -->{% endraw %}
~~~

~~~ ruby
module Jekyll
  class TagIndex < Page
    def initialize(site, base, dir, tag)
      @site = site
      @base = base
      @dir = dir
      @name = 'index.html'
      self.process(@name)
      self.read_yaml(File.join(base, '_layouts'), 'tag_index.html')
      self.data['tag'] = tag
      tag_title_prefix = site.config['tag_title_prefix'] || 'Tagged: '
      tag_title_suffix = site.config['tag_title_suffix'] || '&#8211;'
      self.data['title'] = "#{tag_title_prefix}#{tag}"
      self.data['description'] = "An archive of posts tagged #{tag}."
    end
  end
end
~~~

