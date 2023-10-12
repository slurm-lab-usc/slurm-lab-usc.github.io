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
            web_url: https://slurm-lab.github.io/
          - name: To Be Decided
            photo_url: /img/USC_Slogan.png
            web_url: https://slurm-lab.github.io/

  - name: Master's Students
    list:
      - full: true
        list:
          - name: Vishesh Mittal
            photo_url: /img/people/VisheshMittal.jpg
            web_url: https://vishesh-mittal.github.io/
          - name: To Be Decided
            photo_url: /img/USC_Slogan.png
            web_url: https://slurm-lab.github.io/
          - name: To Be Decided
            photo_url: /img/USC_Slogan.png
            web_url: https://slurm-lab.github.io/
          - name: To Be Decided
            photo_url: /img/USC_Slogan.png
            web_url: https://slurm-lab.github.io/
          - name: To Be Decided
            photo_url: /img/USC_Slogan.png
            web_url: https://slurm-lab.github.io/

  - name: Undergraduate Students
    list:
      - full: true
        list:
          - name: To Be Decided
            photo_url: /img/USC_Slogan.png
            web_url: https://slurm-lab.github.io/

  - name: Faculty
    list:
      - full: true
        list:
          - name: Daniel Seita
            photo_url: https://danielseita.github.io/images/photos/Daniel_DTLA_Aug_2023.png
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
