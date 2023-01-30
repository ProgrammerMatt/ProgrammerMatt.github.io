---
layout: page
title: Movies & TV
---

<style>
    li {
        margin-bottom: 5px;
    }
</style>

{% assign pastShows = site.data.television
        | sort: "title"
%}
{% for show in pastShows %}
  <b>{{ show.title }}</b>
{% if show.rating %}  * My rating: {{ show.rating }}{% endif %}
{% if show.summary %}  * Summary: {{ show.summary }}{% endif %}
{% endfor %}