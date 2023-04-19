---
layout: default
---

Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](./another-page.html).

There should be whitespace between paragraphs.

There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project.

# Header 1

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

## Header 2

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
<div class="posts">

  {% for post in paginator.posts %}

      <h2>
          <a href="{{ post.url }}">{{ post.title }}</a>
      </h2>
      <p>
		<span class="glyphicon glyphicon-time"></span> {{ post.date | date_to_string }}
		{% assign author = site.data.authors[page.author] %}
		{% if author %}
		 &bull; 
		<span class="glyphicon glyphicon-user"></span> <a href="{{ author.web }}">{{ author.name }}</a>
		{% endif %}
	  </p>
      <ul class="tags">
      {% for tag in post.tags %}
        <li><a href="/tags#{{ tag }}" class="tag">{{ tag }}</a></li>
      {% endfor %}
      </ul>
      <hr>
      <p>{{ post.excerpt }}</p>
      <a class="btn btn-primary" href="{{ site.baseurl }}{{ post.url }}">Read More <span class="glyphicon glyphicon-chevron-right"></span></a>
      <hr>

  {% endfor %}

  <!-- Pager -->
  {% if paginator.total_pages > 1 %}
  <ul class="pager">
    {% if paginator.previous_page %}
      <li class="previous">
        <a href="{{ paginator.previous_page_path | prepend: site.baseurl | replace: '//', '/' }}">&larr; Newer</a>
      </li>
    {% else %}
      <li class="previous">
        <span>&larr; Newer</span>
      </li>
    {% endif %}


    {% if paginator.next_page %}
      <li class="next">
        <a href="{{ paginator.next_page_path | prepend: site.baseurl | replace: '//', '/' }}">Older &rarr;</a>
      </li>
    {% else %}
      <li class="next">
        <span>Older &rarr;</span>
      </li>
    {% endif %}
  </ul>
  {% endif %}
</div>
