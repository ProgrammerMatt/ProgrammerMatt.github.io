---
layout: page
title: Movies & TV
---
This is mostly to serve a reminder to me for which movies I've actually watched. I have a poor memory so want a way to reflect.
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