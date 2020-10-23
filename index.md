---
layout: index
title: Home
---
I am a Ph.D. candidate in Electrical and Computer Engineering at Carnegie Mellon University (CMU), advised by [Vyas Sekar](http://users.ece.cmu.edu/~vsekar/){:target="\_blank"}, 
and am part of [CyLab](https://www.cylab.cmu.edu/){:target="\_blank"}, CMU’s Security and Privacy Institute. Before starting at CMU in 2014, I earned bachelor’s degree in Electrical Engineering from the [University of Waterloo](https://uwaterloo.ca/){:target="\_blank"}, Canada.

My research interests lie in the intersection of network security and computer networking. My research work currently focuses on network modeling, network verification, and uncovering security vulnerabilities in network protocols and devices. Recently, I have been looking at enabling black-box analysis of network devices and protocols. My vision is to equip operators and defenders with tools for precisely analyzing and securing networks containing these devices. 



My research work has been recognized with the [NSA Best Scientific Cybersecurity Paper Award](https://www.ece.cmu.edu/news-and-events/story/2016/10/cylab-wins-nsas-best-scientific-cybersecurity-paper-competition.html) and the CSAW Applied Security Research Prize. I am also the  an invited participant at the [2019 EECS Rising Stars workshop](https://publish.illinois.edu/rising-stars/soo-jin-moon/). 




<!-- 
I am a Ph.D. candidate in the ECE department at Carnegie Mellon University, where I am part of [Cylab](https://www.cylab.cmu.edu/). My research interest spans across network and systems security. I am fortunate to be advised by [Vyas Sekar](http://users.ece.cmu.edu/~vsekar/).

Prior to joining CMU, I received a BASc in Electrical Engineering from [University of Waterloo](https://uwaterloo.ca/), ON, Canada. I also have worked in a number of different engineering and programming positions at a variety of organizations. -->


## News 
{%- assign news = site.data.news -%}

{% for n in news %}
**{{ n.date }}** : {{n.content}} {% if n.link %} [[Link]]({{ n.link}}){:target="\_blank"}{% endif %}   
{% endfor %}


## Publications
<!-- ### Under Submission
{%- assign under_sub = site.data.under_submission -%}

{% for pub in under_sub %}
{{ forloop.index }}.  {{ pub.title }}  
{{ pub.authors }}  
{% endfor %}  -->


### Conference and Workshop Papers
{%- assign publications = site.data.publications -%}
{%- assign papers_dir = "/assets/papers/" -%}
{%- assign slides_dir = "/assets/slides/" -%}


{% for pub in publications %}
{{ forloop.index }}.  {{ pub.title }}  
{{ pub.authors }}  
{{ pub.venue_prefix }} [{{ pub.venue }}, {{ pub.year }}]({{ pub.venue_link }})  
{% if pub.paper %}[[Paper]]({{ papers_dir | prepend: site.baseurl | append: pub.paper }}){% endif %}
{% if pub.slides %}[[Slides]]({{ slides_dir | prepend: site.baseurl | append: pub.slides }}){% endif %}
{% if pub.talk_video %}[[Talk Video]]({{ pub.talk_video}}){% endif %}
{% if pub.award1 %} **<span style="color:red">{{ pub.award1}}</span>** [[Link]]({{pub.award1link}}){:target="\_blank"} {% endif %} 
{% if pub.award2 %} **<span style="color:red">{{ pub.award2}}</span>** [[Link]]({{pub.award2link}}){:target="\_blank"} {% endif %} 
{% endfor %} 


<!-- #### Workshop Papers -->
<!-- 
## Professional
{%- assign positions = site.data.professional -%}

{%- for position in positions %}
* {{ position.title }}, [{{ position.employer }}]({{ position.link }}). {{ position.start }}–{{ position.end }}
{%- endfor %} -->


<!-- 
## Teaching
{%- assign schools = site.data.teaching | map: "school" | uniq -%}

{% for school in schools %}
#### {{ school }}
{%- assign positions = site.data.teaching | where: "school", school -%}

{%- for position in positions %}
* {{ position.title }} for [{{ position.course }}]({{ position.link }}). {{ position.semesters }}
{%- endfor %}
{% endfor %} -->

