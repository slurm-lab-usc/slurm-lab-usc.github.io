---
layout: page
title: Members
subtitle:
members:
  - name: PhD Students
    list:
      - full: true
        list:
          - name: Minjune Hwang
            photo_url: /img/people/MinjuneHwang.png
            web_url: https://mj-hwang.github.io/
          - name: Zeyu Shangguan
            photo_url: /img/people/ZeyuShangguan.jpeg
            web_url: https://zshanggu.github.io/
          - name: Yunshuang Li
            photo_url: /img/people/Yunshuang.jpeg
            web_url: https://li-yunshuang.github.io/
          - name: Yiyang Ling
            photo_url: /img/people/Yiyang.jpg
            web_url: https://yiyang0207.github.io/
  - name: Master's Students
    list:
      - full: true
        list:
          - name: Anupam Patil
            photo_url: /img/people/AnupamPatil.jpeg
            web_url: https://www.linkedin.com/in/anupam-patil-114b841b0/
          - name: Dhanush Penmetsa
            photo_url: /img/USC_Slogan.png
            web_url: https://slurm-lab-usc.github.io/
          - name: Vedant Raval
            photo_url: /img/people/VedantRaval.jpeg
            web_url: https://www.linkedin.com/in/vedantraval23/
          - name: Yuhai Wang
            photo_url: /img/people/Yuhai.jpg
            web_url: https://yuhaiw.github.io/
          - name: Karan Owalekar
            photo_url: /img/people/karanOwalekar.jpg
            web_url: https://www.linkedin.com/in/karan-owalekar/
          - name: Enyu Zhao
            photo_url: /img/people/Enyu.jpeg
            web_url: https://www.linkedin.com/in/enyu-zhao-564566250/
          - name: Charlene Yuen
            photo_url: /img/people/Charlene.jpg
            web_url: https://lazerbird.github.io/
          - name: Harshitha B R
            photo_url: /img/people/HBR.JPG
            web_url: https://www.linkedin.com/in/harshitha-b-r-2ab510190/

  - name: Undergraduate Students
    list:
      - full: true
        list:
          - name: Hao Jiang
            photo_url: /img/people/HaoJiang.jpg
            web_url: https://linkedin.com/in/hao-jiang-1a3a73225
          - name: Oluwatobiloba Adesanya
            photo_url: /img/people/TobiAdesanya.jpeg
            web_url: https://www.linkedin.com/in/oluwatobilobaadesanya   
          - name: Peter Wang
            photo_url: /img/people/PeterWang.png
            web_url: https://pwang649.github.io/
          - name: Jonathan Ong
            photo_url: /img/people/JonathanOng.jpg
            web_url: https://www.linkedin.com/in/ongjonathand
          - name: Vijay Kumaravelrajan
            photo_url: /img/people/VijayKumaravelrajan.jpg
            web_url: https://www.linkedin.com/in/vijay-kumaravelrajan/
          - name: Anisha Chitta
            photo_url: /img/people/AnishaChitta.jpg
            web_url: https://www.linkedin.com/in/anisha-chitta/

  - name: Interns and Visitors
    list:
      - full: true
        list:
          - name: Kartika Santoso
            photo_url: /img/people/KartikaSantoso.jpg
            web_url: https://www.linkedin.com/in/kartika-s/

  - name: Faculty
    list:
      - full: true
        list:
          - name: Daniel Seita
            photo_url: /img/people/Daniel_2023_square.png
            web_url: https://danielseita.github.io/

  - name: <a name="alumni"></a>Alumni
    # list:
    #   - name: PhD alumni
    #     full: False
    #     list:
    #       - name: Siddharth Ancha (co-advised with Srinivasa Narasimhan) -> Post-doc with Nick Roy at MIT
    #         web_url: https://siddancha.github.io/
    #       - name: Xingyu Lin -> Post-doc with Pieter Abbeel at UC Berkeley
    #         web_url: https://xingyu-lin.github.io/
    #       - name: Brian Okorn (co-advised with Martial Hebert) -> Boston Dynamics AI Institute
    #         web_url: https://www.ri.cmu.edu/ri-people/brian-e-okorn/

---

<div class="row">
  {% for big_group in page.members %}
    <h1> {{big_group.name}} </h1>
    {% for group in big_group.list %}
    {% if group.list.size > 0 %}
      {% if group.name %}
        <h2>{{ group.name }}</h2>
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
