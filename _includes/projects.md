<h2 id="projects" style="margin: 2px 0px -15px;">Projects</h2>

<div class="publications">
<ol class="bibliography">

{% for project in site.data.projects.main %}

<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    {% if project.image %} 
    <img src="{{ project.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
    {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative; padding-right: 15px; padding-left: 15px;">
      <div class="title"><a href="{{ project.link }}">{{ project.title }}</a></div>
  </div>
</div>
</li>

<br>

{% endfor %}

</ol>
</div>
