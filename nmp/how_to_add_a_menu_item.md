---
permalink: /how-to-add-a-menu-item/
title: "How to add a menu item in AcademicPages template"
author_profile: true
redirect_from: 
  - "/nmp/"
  - "/nmp.html"
---

How to add a menu item in Academic Pages template.
I will explain how I added a menu item named "Journal".

Add a page
======
Add a journal.html file to the _pages folder.  Inside that file put this: 
```
---
permalink: /journal/
title: "Journal"
---


{% include base_path %}


{% for post in site.journal %}
  {% include archive-single.html %}
{% endfor %}
```

Add a folder
======
Add the folder _journal in the root of the site.

Edit _data/navigation.yml
======
add this:
```
  - title: "Journal"
    url: /journal/
```

Edit _config.yml
======
In _config.yml find the section "collections" and add this to the bottom:
```
  journal:
    output: true
    permalink: /:collection/:path/
```
So that this section looks like this:
```
collections:
  teaching:
    output: true
    permalink: /:collection/:path/
  publications:
    output: true
    permalink: /:collection/:path/
  portfolio:
    output: true
    permalink: /:collection/:path/
  talks:
    output: true
    permalink: /:collection/:path/
  journal:
    output: true
    permalink: /:collection/:path/
```
Now look for the section named "default".  For me it is the section right below "collections".
Add this to the bottom of it:
```
  # _journal
  - scope:
      path: ""
      type: journal
    values:
      layout: single
      author_profile: true
      share: true
      comment: true
```
So that the section looks like this:
```
defaults:
  # _posts
  - scope:
      path: ""
      type: posts
    values:
      layout: single
      author_profile: true
      read_time: true
      comments: true
      share: true
      related: true
  # _pages
  - scope:
      path: ""
      type: pages
    values:
      layout: single
      author_profile: true
  # _teaching
  - scope:
      path: ""
      type: teaching
    values:
      layout: single
      author_profile: true
      share: true
      comments: true
  # _publications
  - scope:
      path: ""
      type: publications
    values:
      layout: single
      author_profile: true
      share: true
      comments: true
  # _portfolio
  - scope:
      path: ""
      type: portfolio
    values:
      layout: single
      author_profile: true
      share: true
      comment: true
  # _talks
  - scope:
      path: ""
      type: talks
    values:
      layout: talk
      author_profile: true
      share: true
  # _journal
  - scope:
      path: ""
      type: journal
    values:
      layout: single
      author_profile: true
      share: true
      comment: true
```

Add content
======
Now, lets add our content.  Put a file named something.md.  For my example I'm going to add a filenamed: cybr-1100-week01.md.  Inside this file we need to have:
```
---
title: "CYBR-1100 Week 01"
collection: journal
permalink: /journal/cybr-1100-week01
---

This is a description of a journal. You can use markdown like any other post.

Heading 1
======

Heading 2
======

Heading 3
======
```
Now just keep adding files with this data inside to the folder, and your golden.
