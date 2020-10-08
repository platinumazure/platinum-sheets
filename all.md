---
layout: default
title: All Posts
---
# All Posts

Here are all of the posts on Platinum Sheets!

{% capture group_expression %}post.date | date: "%B %Y" {% endcapture %}
{% assign post_groups = site.posts | group_by_exp: "post", group_expression %}

{% for post_group in post_groups %}
## {{ post_group.name }}

{% for post in post_group.items -%}
* [{{ post.title }}]({{ post.url | relative_url }}) ({{ post.date | date:"%-d %B %Y" }})
{% endfor %}

{% endfor %}
