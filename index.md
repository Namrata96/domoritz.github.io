---
layout: page
title: "Home"
class: home
---

# Hi, I'm Namrata Mukhija

<div class="columns" markdown="1">

<div class="intro" markdown="1">
I'm a current student pursuing a M.S. in Computer Science at [New York University, Courant School of Mathematical Sciences](https://www.courant.nyu.edu/). I recently interned at J.P Morgan and Chase & Co. as a Applied NLP researcher in the [Machine Learning Center of Excellence](https://www.jpmorgan.com/technology/applied-ai-and-ml). My work was center at assesing the effect of paraphrasing as a data augmentation tool in improving downstream Named Entity Recognition problem in low versus high resource scenarios. I previously interned at [Microsoft Research, India](https://www.microsoft.com/en-us/research/lab/microsoft-research-india/) under [Dr. Kalika Bali](https://www.microsoft.com/en-us/research/people/kalikab/) and [Dr. Monojit Choudhury](https://www.microsoft.com/en-us/research/people/monojitc/) in developing a [framework](https://arxiv.org/abs/2110.07444) for prioritizing research for low-resource language communities, understanding different [dilemmas](https://dl.acm.org/doi/10.1145/3530190.3534792) faced by technologists, their origin and complexity, and involving low-resource language communities in the development of language technologies. I was previously a Software Engineer at [Microsoft](https://www.microsoft.com/). I was involved in developing various products such as [PowerPoint](https://www.microsoft.com/en-in/microsoft-365/powerpoint), [Fluid Framework](https://fluidframework.com/), and [Unified Service Desk](https://docs.microsoft.com/en-us/dynamics365/unified-service-desk/admin/overview-unified-service-desk?view=dynamics-usd-4.1).

I received my B.E. in Information Technology from [Netaji Subhas University of Technology](http://www.nsit.ac.in/).

I was awarded the Microsoft Experiences+Devices India Leadership Award 2020 across 2500+ employees for generating energy in the team, demonstrating ”All for One, One for All” mindset, and championing diversity and inclusion.

I actively work and volunteer for non-profits working towards closing the gender gap across industries - [Women in AI](http://www.womeninai.co/) where I lead the Women in AI India chapter, [Thousand Eyes On Me](http://www.thousandeyeson.me) where I work as the Program Director. If you have an idea that could help reduce the gender gap, please <a href="mailto:namrata@womeninai.co">reach out</a> to me!
</div>

<div class="me" markdown="1">
<picture>
  <img
    src='/images/namrata.jpg'
    alt='Namrata Mukhija'/>
</picture>

{:.no-list}
* <a href="mailto:{{ site.email }}">{{ site.email }}</a>
</div>

</div>

## Featured Projects

<div class="featured-projects">
  {% assign sorted_projects = site.data.projects | sort: 'highlight' %}
  {% for project in sorted_projects %}
    {% if project.highlight %}
      {% include project.html project=project %}
    {% endif %}
  {% endfor %}
</div>
<a href="{{ "/projects/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show More Projects
</a>

<!-- ## Featured Publications -->

<!-- <div class="featured-publications">
  {% for pub in site.publications %}
    {% if pub.highlight %}
      <a href="{{ pub.pdf }}" class="publication">
        <strong>{{ pub.title }}</strong>
        <span class="authors">{% for author in pub.authors %}{{ author }}{% unless forloop.last %}, {% endunless %}{% endfor %}</span>.
        <i>{{ pub.venue }}, {{ pub.year }}</i>.
        {% for award in pub.awards %}<br/><span class="award"><i class="fas fa-{% if award == "Best Paper Award" %}trophy{% else %}award{% endif %}" aria-hidden="true"></i> {{ award }}</span>{% endfor %}
      </a>
    {% endif %}
  {% endfor %}
</div>

<a href="{{ "/publications/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show All Publications
</a>

<div class="news-travel" markdown="1">

<div class="news" markdown="1">
## Latest News

<ul>
{% for news in site.data.news limit:10 %}
  {% include news.html news=news %}
{% endfor %}
</ul>

</div>

<div class="travel" markdown="1">
## Latest Travel

<table>
<tbody>
{% assign future_travel = site.data.travel | where_exp:'item','item.start == null' %}
{% for travel in future_travel %}
  {% include travel.html travel=travel %}
{% endfor %}
{% assign sorted_travel = site.data.travel | where_exp:'item','item.start' | sort: 'start' | reverse %}
{% for travel in sorted_travel limit:10 %}
  {% include travel.html travel=travel %}
{% endfor %}
</tbody>
</table>

</div> -->

<!-- </div> -->
