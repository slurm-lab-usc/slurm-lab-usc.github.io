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
            photo_url: https://slurm-lab-usc.github.io/img/people/MinjuneHwang.png
            web_url: https://mj-hwang.github.io/
          - name: Zeyu Shangguan
            photo_url: https://slurm-lab-usc.github.io/img/people/ZeyuShangguan.jpeg
            web_url: https://zshanggu.github.io/
          - name: Yunshuang Li
            photo_url: https://slurm-lab-usc.github.io/img/people/Yunshuang.jpeg
            web_url: https://li-yunshuang.github.io/
          - name: Yiyang Ling
            photo_url: https://slurm-lab-usc.github.io/img/people/Yiyang.jpg
            web_url: https://yiyang0207.github.io/

  - name: Master's Students
    list:
      - full: true
        list:
          - name: Anupam Patil
            photo_url: https://slurm-lab-usc.github.io/img/people/AnupamPatil.jpeg
            web_url: https://www.linkedin.com/in/anupam-patil-114b841b0/
          - name: Dhanush Penmetsa
            photo_url: https://slurm-lab-usc.github.io/img/USC_Slogan.png
            web_url: https://slurm-lab-usc.github.io/
          - name: Vedant Raval
            photo_url: https://slurm-lab-usc.github.io/img/people/VedantRaval.jpeg
            web_url: https://www.linkedin.com/in/vedantraval23/
          - name: Yuhai Wang
            photo_url: https://slurm-lab-usc.github.io/img/people/Yuhai.jpg
            web_url: https://yuhaiw.github.io/
          - name: Karan Owalekar
            photo_url: https://slurm-lab-usc.github.io/img/people/karanOwalekar.jpg
            web_url: https://www.linkedin.com/in/karan-owalekar/
          - name: Enyu Zhao
            photo_url: https://slurm-lab-usc.github.io/img/people/Enyu.jpeg
            web_url: https://www.linkedin.com/in/enyu-zhao-564566250/
          - name: Charlene Yuen
            photo_url: https://slurm-lab-usc.github.io/img/people/Charlene.jpg
            web_url: https://lazerbird.github.io/
          - name: Harshitha B R
            photo_url: https://slurm-lab-usc.github.io/img/people/HBR.JPG
            web_url: https://www.linkedin.com/in/harshitha-b-r-2ab510190/
          - name: Hanyang Zhou
            photo_url: https://slurm-lab-usc.github.io/img/people/HanyangZHOU.png
            web_url: https://www.linkedin.com/in/hanyang-zhou-usc
          - name: Sicheng He
            photo_url: https://slurm-lab-usc.github.io/img/people/hesicheng.jpg
            web_url: https://hesic73.github.io/
          - name: Jonathan Zamora
            photo_url: https://slurm-lab-usc.github.io/img/people/jonzamora.jpg
            web_url: https://jonzamora.dev/

  - name: Undergraduate Students
    list:
      - full: true
        list:
          - name: Hao Jiang
            photo_url: https://slurm-lab-usc.github.io/img/people/HaoJiang.jpg
            web_url: https://linkedin.com/in/hao-jiang-1a3a73225
          - name: Oluwatobiloba Adesanya
            photo_url: https://slurm-lab-usc.github.io/img/people/TobiAdesanya.jpeg
            web_url: https://www.linkedin.com/in/oluwatobilobaadesanya
          - name: Jonathan Ong
            photo_url: https://slurm-lab-usc.github.io/img/people/JonathanOng.jpg
            web_url: https://www.linkedin.com/in/ongjonathand
          - name: Vijay Kumaravelrajan
            photo_url: https://slurm-lab-usc.github.io/img/people/VijayKumaravelrajan.jpg
            web_url: https://www.linkedin.com/in/vijay-kumaravelrajan/
          - name: Zitong Huang
            photo_url: https://slurm-lab-usc.github.io/img/people/Cynthia.jpeg
            web_url: https://www.linkedin.com/in/zitong-huang/
          - name: Anisha Chitta
            photo_url: https://slurm-lab-usc.github.io/img/people/AnishaChitta.jpeg
            web_url: https://www.linkedin.com/in/anisha-chitta/
          - name: Letian Zhang
            photo_url: https://slurm-lab-usc.github.io/img/people/LetianZhang.jpeg
            web_url: https://www.linkedin.com/in/letian-zhang-630b37235/

  - name: Interns and Visitors
    list:
      - full: true
        list:
          - name: Gayathri Rajesh
            photo_url: https://slurm-lab-usc.github.io/img/USC_Slogan.png
            web_url: https://slurm-lab-usc.github.io/
          - name: Abhinav Pillai
            photo_url: https://slurm-lab-usc.github.io/img/USC_Slogan.png
            web_url: https://slurm-lab-usc.github.io/
          - name: Ebonee Davis
            photo_url: https://slurm-lab-usc.github.io/img/USC_Slogan.png
            web_url: https://slurm-lab-usc.github.io/

  - name: Faculty
    list:
      - full: true
        list:
          - name: Daniel Seita
            photo_url: https://slurm-lab-usc.github.io/img/people/Daniel_2023_square.png
            web_url: https://danielseita.github.io/

  # - name: Alumni
  #   web_url: https://slurm-lab-usc.github.io/alumni/

  - name: Alumni
    list:
      - name: Undergraduate students
        full: False
        list:
          - name: Qian (Peter) Wang -> Yale University, PhD in CS
            web_url: https://pwang649.github.io/
      - name: Visitors
        full: False
        list:
          - name: Ce (Chris) Wang -> SWE at Ambarella Inc
            web_url: https://www.linkedin.com/in/wangce94/
---

<div class="row">
  {% for big_group in page.members %}
    {% if big_group.web_url %}
      <h1> <a href="{{big_group.web_url}}"> {{big_group.name}} </a> </h1>
    {% else %}
      <h1> {{big_group.name}} </h1>
      {% for group in big_group.list %}
        {% if group.list.size > 0 %}
          {% if group.name %}
            <h2 style="text-align: left; margin-bottom: 20px;"> {{ group.name }} </h2>
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
    {% endif %}
  {% endfor %}
</div>
