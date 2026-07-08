---
layout: page
title: Broader Impacts
# slim: true

broader_impacts:
  - semester: Summer 2026
    list:
      - month: July
        list:
          - event: USC Robotics REU Tour at JPL
            photo_url: /img/broader_impacts/2026_July_JPL_01.jpeg‎
          - event: USC Robotics REU Tour at JPL
            photo_url: /img/broader_impacts/2026_July_JPL_02.jpeg‎
  
  - semester: Spring 2025
    list:
      - month: April
        list:
          - event: Lab tours (ARX5 demo)
            photo_url: /img/broader_impacts/IMG_8140_Ayano.jpeg
          - event: Lab tours (UR5 demo)
            photo_url: /img/broader_impacts/IMG_8131_Zeyu.jpeg
  
  - semester: Summer 2024
    list:
      - month: July
        list:
          - event: USC Robotics REU Tour at JPL
            photo_url: /img/broader_impacts/2024_July_JPL_02.png
          - event: USC Robotics REU Tour at JPL
            photo_url: /img/broader_impacts/2024_July_JPL_01.png

---

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

