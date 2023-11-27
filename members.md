---
layout: page
title: Members
subtitle:
members:
  - name: PhD Students
    list:
      - full: true
        list:
          - name: To Be Decided
            photo_url: /img/USC_Slogan.png
            web_url: https://slurm-lab-usc.github.io/

  - name: Master's Students
    list:
      - full: true
        list:
          - name: Vishesh Mittal
            photo_url: /img/people/VisheshMittal.jpg
            web_url: https://vishesh-mittal.github.io/
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
          - name: Kriti Asija
            photo_url: /img/people/KritiAsija.jpg
            web_url: https://www.linkedin.com/in/kriti-asija-72638a176/

  - name: Undergraduate Students
    list:
      - full: true
        list:
          - name: Hao Jiang
            photo_url: /img/USC_Slogan.png
            web_url: https://slurm-lab-usc.github.io/
          - name: Emily Zhu
            photo_url: /img/people/EmilyZhu.JPG
            web_url: https://github.com/emilyzhu2027

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
