---
layout: page
title: Alumni
subtitle:
members:
  - name: Undergraduate students
    list:
      - full: false
        list:
          - name: Qian (Peter) Wang -> Yale University CS PhD
            web_url: https://pwang649.github.io/
---

<div class="row">
  {% for big_group in page.members %}
    <h1> {{big_group.name}} </h1>
    {% for group in big_group.list %}
    {% if group.list.size > 0 %}
      {% if group.name %}
        <h2> {{ group.name }} </h2>
      {% endif %}
      {% if group.full %}
      <div class="row member-row">
        {% for member in group.list %}
          <div class="col-xl-3 col-lg-3 col-md-3 text-center col-sm-6 col-xs-6 member-col">
            <a target="_blank" href="{{ member.web_url }}">
              <img class="img-responsive" src="{{ member.photo_url }}" alt="{{member.name}}">
            </a>
            <a target="_blank" href="{{ member.web_url }}">
              {{ member.name }}
            </a>
          </div>
        {% endfor %}
      </div>
      {% else %}
        <ul>
          {% for member in group.list %}
            {% if member.web_url %}
              <li><a href="{{member.web_url}}"> {{member.name}} </a></li>
            {% else %}
              <li><a> {{member.name}} </a></li>
            {% endif %}
          {% endfor %}
        </ul>
      {% endif %}
    <br>
    {% endif %}
    {% endfor %}
  {% endfor %}
</div>


<!-- <h3 id="undergraduate-students">Undergraduate students</h3>
<ul>
</ul>
</div> -->

<!-- <h2 id="collaborators">Collaborators</h2> -->
<!-- <ul>
  <li><a href="https://www.cs.cmu.edu/~astein/">Aaron Steinfeld</a></li>
  <li><a href="https://www.cs.cmu.edu/~kkitani/">Kris Kitani</a></li>
  <li><a href="http://www.lauravherlant.com/">Laura Herlant</a></li>
</ul> -->