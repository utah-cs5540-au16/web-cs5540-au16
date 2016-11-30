---
layout: base/bar-sidebar-none
title: Projects

projects:
- name: Distraction Killer
  path: distractionkiller 
- name: Team Pet Care
  path: team_pet_care
- name: Perfect Timing
  path: perfect_timing
- name: Inkweaver
  path: brostronauts
- name: Carepool
  path: carepool
- name: EdHub Boards
  path: edhub_boards
- name: Food Scanner
  path: food_scanner
- name: NRGY
  path: nrgy
- name: PrepAIrd
  path: prepaird
- name: SBO
  path: SBO
- name: Smart Shopper
  path: SmartShopper
- name: Time Saver
  path: time_saver
   
---

<html>
<div class="row">
<div class="col-md-9" markdown="block">
	

{% assign projects_rows = page.projects | size | divided_by: 4 %}

<div class="row">
  {% for item_project in page.projects %}
    <div class="col-sm-3 col-xs-6">        
      <p>
        <a href="{{ site.baseurl }}/projects/{{ item_project.path }}/" target="_blank">
          {{ item_project.name }}
        </a>
      </p>
      <div class="thumbnailBox">
        <a href="{{ site.baseurl }}/projects/{{ item_project.path }}/" target="_blank">
          <img src="{{ site.baseurl }}/projects/{{ item_project.path }}/project_thumb.png" width="150" class="projectThumbnail" alt="{{ item_project.name }}"/>
        </a>
      </div>
      {% assign row_current = forloop.index | minus: 1 | divided_by: 4 | plus: 1 %}
      {% unless row_current == projects_rows %}
        <p>&nbsp;</p>
      {% endunless %}
    </div>
  {% endfor %}
</div>

</div>

{% comment %}
<div class="col-md-3 hidden-xs hidden-sm" markdown="block">
<div class="panel panel-default" style="margin-top:20px;">

<div class="panel-heading" markdown="block">
	

## Poster Session
</div>
<div class="panel-body" markdown="block">
Please join us for a poster session celebrating the outstanding design work of CSE 440 students:
  
Tuesday, June 7
  
12:30 pm
    
[CSE Atrium](http://www.washington.edu/maps/#!/cse)
Thank you for joining us to celebrate the outstanding design work of CSE 440 students:

Tuesday, June 7
  
12:30 pm

<img src="{{ site.baseurl }}/images/poster_session.jpg" width="100%" alt="Poster Session"/>

</div>

</div>
{% endcomment %}
</div>
</div>
</html>