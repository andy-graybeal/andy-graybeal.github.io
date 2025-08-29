---
permalink: /how-to-add-a-menu-item/
title: "How to add a menu item in AcademicPages template"
author_profile: true
redirect_from: 
  - "/nmp/"
  - "/nmp.html"
---

How to add a menu item in Academic Pages template
I will explain how to add a menu item named "Journal"

Add a page
======
Add a journal.html file to the _pages folder.  Inside that file put this: 
---
permalink: /journal/
title: "Journal"
---


{% include base_path %}


{% for post in site.journal %}
  {% include archive-single.html %}
{% endfor %}


Add a folder
======

Add a nav menu item
======

Edit _config.yml
======

Add content
======
