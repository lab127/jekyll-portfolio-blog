---
layout: page
title: Credit
---

<h3>Design and framework</h3>
<table class="table">
  {% for cred in site.data.credit.creds%}
  <tr>
    <td>{{ cred.for }}</td>
    {% if cred.url %}
    <td><a target="_blank" href="{{ cred.url }}">{{ cred.by }}</a></td>
    {% else %}
    <td>{{ cred.by }}</td>
    {% endif %}
    <td>
      {% if cred.lic %}
        {{ site.data.credits.licenses[cred.lic].name }}
      {% endif %}
    </td>
  </tr>
  {% endfor %}
</table>

<h3>Images</h3>
<div class="row">
  {% for image in site.data.credit.image-credit %}
  <div class="col-lg-3 col-md-6 col-sm-6">
    <img src="{{ image.src }}">
    <p class="text-center">{{ site.data.credits.licenses[image.lic].name }}</p>
    <p><a href="{{ image.url }}">{{ image.by }}</a></p>
  </div> 
  {% endfor %}
</div>
