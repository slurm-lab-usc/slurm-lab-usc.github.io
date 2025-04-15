---
layout: page
title: Broader Impacts
# slim: true

broader_impacts:
  - semester: Spring 2025
    list:
      - month: April
        list:
          - event: Lab tours (ARX5 demo)
            photo_url: /img/broader_impacts/IMG_8140_Ayano.jpeg
          - event: Lab tours (UR5 demo)
            photo_url: /img/broader_impacts/IMG_8131_Zeyu.jpeg
  
---

<!-- ## Summer 2024
### August

<div style="display: flex; justify-content: space-between; align-items: center;">  
    <div style="flex: 1;">  
        <img src="/img/broader_impacts/Lab_social.jpeg" alt="Detroit Pizza Depot" style="width: 90%; display: block;">  
        <p style="text-align: center; margin-top: 10px;">Detroit Pizza Depot</p>  
    </div>  
    <div style="flex: 1;">  
        <img src="/img/broader_impacts/Birthday.jpeg" alt="Happy birthday to Daniel!" style="width: 90%; display: block;">  
        <p style="text-align: center; margin-top: 10px;">Happy birthday to Daniel!🎂</p>  
    </div>  
</div> -->

<div class="row">
  {% for big_group in page.broader_impacts %}
    <h1> {{big_group.semester}} </h1>
    {% for group in big_group.list %}
      {% if group.list.size > 0 %}
        {% if group.month %}
          <h2 style="text-align: left; margin-bottom: 20px;"> {{ group.month }} </h2>
        {% endif %}
        <div class="row broader_impacts-row">  
          {% for broader_impacts in group.list %}  
            <div class="col-xl-6 col-lg-6 col-md-6 text-center col-sm-12 col-xs-12 broader_impacts-col">  
              <img class="lab-photo img-responsive" src="{{ broader_impacts.photo_url }}" alt="{{ broader_impacts.event }}">    
              <div class="photo-caption">{{ broader_impacts.event }}</div>  
            </div>  
          {% endfor %}  
        </div>
      <br>
      {% endif %}
    {% endfor %}
  {% endfor %}
</div>

