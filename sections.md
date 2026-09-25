---
layout: page
title: Archive
permalink: /archive
---

# Archives (by section)

Published pieces are sorted into sections, or "categories" as they are known in the blogging world. The following sections are offered, and each publication item is organised into their respective section.

<hr />
<br />

{% for section in site.data.sections %}
  <h3 class="post-meta" style="color:black;"> Section on: <i>{{ section.name }}</i></h3>
  <p>{{ section.desc }}</p>
  
{% endfor %}

