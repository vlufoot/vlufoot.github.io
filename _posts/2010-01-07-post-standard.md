---
layout: post
title: "Post: Standard:summary"
excerpt_separator: "<!--more-->"
categories:
  - Data Science
tags:
  - Git
---

**`page.title` example:**

This is the post content. Archive-index pages should display an [auto-generated excerpt](https://jekyllrb.com/docs/posts/#post-excerpts)

## EXCERPT_SEPERATOR


Mrs. Darling first heard of Peter when she was tidying up her children's minds. It is the nightly custom of every good mother after her children are asleep to rummage in their minds and put things straight for next morning, repacking into their proper places the many articles that have wandered during the day.

<!--more-->

This post has a manual excerpt `<!--more-->` set after the second paragraph. The following YAML Front Matter has also be applied:

```yaml
excerpt_separator: "<!--more-->"
```

<!--more-->

## QUOTE

> Only one thing is impossible for God: To find any sense in any copyright law on the planet.
>
> <cite><a href="http://www.brainyquote.com/quotes/quotes/m/marktwain163473.html">Mark Twain</a></cite>

## YOUTOUBE EMBEDDING

<div class="embed-responsive embed-responsive-16by9">
  <iframe width="640" height="360" src="https://www.youtube-nocookie.com/embed/l2Of1-d5E5o?controls=0&amp;" frameborder="0" allowfullscreen></iframe>
</div>

This post tests YouTube video embeds.

Simply wrap embeds with a `<div>` element and the appropriate classes:

```html
<!-- 16:9 aspect ratio -->
<div class="embed-responsive embed-responsive-16by9">
  <iframe class="embed-responsive-item" src="..."></iframe>
</div>

<!-- 4:3 aspect ratio -->
<div class="embed-responsive embed-responsive-4by3">
  <iframe class="embed-responsive-item" src="..."></iframe>
</div>
```

## Tables

| Employee         | Salary |                                                              |
| --------         | ------ | ------------------------------------------------------------ |
| [John Doe](#)    | $1     | Because that's all Steve Jobs needed for a salary.           |
| [Jane Doe](#)    | $100K  | For all the blogging she does.                               |
| [Fred Bloggs](#) | $100M  | Pictures are worth a thousand words, right? So Jane × 1,000. |
| [Jane Bloggs](#) | $100B  | With hair like that?! Enough said.                           |


## Images

Quisque consequat sapien eget quam rhoncus, sit amet laoreet diam tempus. Aliquam aliquam metus erat, a pulvinar turpis suscipit at.

![placeholder](https://placehold.it/800x400 "Large example image")
![placeholder](https://placehold.it/400x200 "Medium example image")
![placeholder](https://placehold.it/200x200 "Small example image")
