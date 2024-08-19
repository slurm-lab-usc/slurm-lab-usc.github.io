---
layout: page
title: Lab Photos
# slim: true

lab_photos:
  - semester: Summer 2024
    list:
      - month: August
        list:
          - event: Detroit Pizza Depot, August 2024
            photo_url: /img/lab_photos/Lab_social.jpg
          - event: Happy birthday to Daniel!🎂
            photo_url: /img/lab_photos/Birthday.jpg
---

<!-- ## Summer 2024
### August

<div style="display: flex; justify-content: space-between; align-items: center;">  
    <div style="flex: 1;">  
        <img src="/img/lab_photos/Lab_social.jpeg" alt="Detroit Pizza Depot" style="width: 90%; display: block;">  
        <p style="text-align: center; margin-top: 10px;">Detroit Pizza Depot</p>  
    </div>  
    <div style="flex: 1;">  
        <img src="/img/lab_photos/Birthday.jpeg" alt="Happy birthday to Daniel!" style="width: 90%; display: block;">  
        <p style="text-align: center; margin-top: 10px;">Happy birthday to Daniel!🎂</p>  
    </div>  
</div> -->

<div class="row">
  {% for big_group in page.lab_photos %}
    <h1> {{big_group.semester}} </h1>
    {% for group in big_group.list %}
      {% if group.list.size > 0 %}
        <!-- {% if group.month %}
          <h2 style="text-align: left; margin-bottom: 20px;"> {{ group.month }} </h2>
        {% endif %} -->
        <div class="row lab_photos-row">
          {% for lab_photos in group.list %}
            <div class="col-xl-6 col-lg-6 col-md-6 text-center col-sm-12 col-xs-12 lab_photos-col">
              <img class="img-responsive" src="{{ lab_photos.photo_url }}" alt="{{lab_photos.event}}">  
            {{ lab_photos.event }}
            </div>
          {% endfor %}
        </div>
      <br>
      {% endif %}
    {% endfor %}
  {% endfor %}
</div>

