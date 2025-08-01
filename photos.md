---
layout: page
title: Lab Photos
# slim: true

lab_photos:
  - semester: Summer 2025
    list:
      - month: July
        list:
          - event: "ISER 2025: Wenhao Liu and Hanyang Zhou during a panel discussion"
            photo_url: /img/lab_photos/ISER1.png
          - event: "ISER 2025: Hiking event with Wenhao, Hanyang, and Daniel"
            photo_url: /img/lab_photos/ISER2.jpg
      - month: June
        list:
          - event: "RSS 2025 🤖 & Volunteers"
            photo_url: /img/lab_photos/RSS1.jpg
          - event: "RSS 2025 🤖 & Volunteers"
            photo_url: /img/lab_photos/RSS2.jpg
  - semester: Spring 2025
    list:
      - month: May
        list:
          - event: "Lab social: 7 wonders"
            photo_url: /img/lab_photos/lab_social_2025_summer.jpg
      - month: March
        list:
          - event: New PhD admits welcome dinner with Geometry, Vision, and Learning Lab
            photo_url: /img/lab_photos/new_PhD_admits_welcome_dinner.JPEG
      - month: February
        list:
          - event: Post-RSS deadline lunch with lead authors
            photo_url: /img/lab_photos/Post_RSS2025.jpg
  - semester: Fall 2024
    list:
      - month: September
        list:
          - event: Welcome Ph.D. students
            photo_url: /img/lab_photos/phd_welcome.jpg
      - month: August
        list:
          - event: Unitree G1 demo
            photo_url: /img/lab_photos/Unitree_G1.jpg
          - event: Unitree Go2 demo
            photo_url: /img/lab_photos/Unitree_Go2.jpg
  - semester: Summer 2024
    list:
      - month: August
        list:
          - event: "Lab social: Detroit Pizza Depot"
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
        {% if group.month %}
          <h2 style="text-align: left; margin-bottom: 20px;"> {{ group.month }} </h2>
        {% endif %}
        <div class="row lab_photos-row">  
          {% for lab_photos in group.list %}  
            <div class="col-xl-6 col-lg-6 col-md-6 text-center col-sm-12 col-xs-12 lab_photos-col">  
              <img class="lab-photo img-responsive" src="{{ lab_photos.photo_url }}" alt="{{ lab_photos.event }}">    
              <div class="photo-caption">{{ lab_photos.event }}</div>  
            </div>  
          {% endfor %}  
        </div>
      <br>
      {% endif %}
    {% endfor %}
  {% endfor %}
</div>

