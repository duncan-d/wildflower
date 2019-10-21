---
layout: narrow
title: Stylists
---
<div class="row">
  {% for stylist in site.stylists %}
  <div class="col mb-5">
    <div style="width: 15rem;" class="card bg-primary mx-auto">
      <div class="text-center d-none d-sm-inline-block">
        <img style="min-width: 125px" class="card-img-top p-3" src="{{ site.baseurl }}/assets/images/{{ stylist.image_link }}" alt="{{ stylist.name }}">
      </div>
      <div class="text-center d-inline-block d-sm-none">
          <img style="max-width: 100px" class="card-img-top pt-2" src="{{ site.baseurl }}/assets/images/{{ stylist.image_link }}" alt="{{ stylist.name }}">
        </div>
      <div class="card-body">
        <div class="card-text">
          <h5>{{ stylist.name }}</h5>
          <p>{{ stylist.content }}</p>
        </div>
      </div>
    </div>
  </div>
  {% endfor %}
</div>
