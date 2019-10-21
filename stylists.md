---
layout: narrow
title: Stylists
---
<div class="row">
  {% assign stylists = site.stylists | sort: 'last_name' | sort: 'position' %}
  {% for stylist in stylists %}
  <!-- Card for small screens/phones -->
  <div class="col mb-5 d-sm-none">
    <a href="{{ site.baseurl }}{{ stylist.url }}">
      <div style="width: 10rem;" class="card bg-primary mx-auto">
        <img style="" class="card-img" src="{{ site.baseurl }}/assets/images/{{ stylist.image_link }}" alt="{{ stylist.name }}">
        <div class="card-img-overlay h-100 d-flex flex-column justify-content-end">
          <div class="card-text text-danger">
            <h5 class="bg-primary border-secondary rounded p-1 m-0 text-center">{{ stylist.first_name }} - {{ stylist.position }}</h5>
          </div>
        </div>
      </div>
    </a>
  </div>
  <!-- card for larger screens -->
  <div class="col mb-5 d-none d-sm-inline">
    <div style="width: 15rem;" class="card bg-primary mx-auto">
      <a href="{{ site.baseurl }}{{ stylist.url }}">
        <img style="" class="card-img-top" src="{{ site.baseurl }}/assets/images/{{ stylist.image_link }}" alt="{{ stylist.name }}">
      </a>
      <div class="card-body">
        <div class="card-text">
          <h5 class="bg-primary border-secondary rounded p-1 m-0 text-center">{{ stylist.first_name }} {{ stylist.last_name }} - {{ stylist.position }}</h5>
          <p>{{ stylist.blurb }}</p>
          <a class="btn btn-dark text-light w-100 text-center" href="mailto:{{ stylist.email }}">Email {{ stylist.first_name }}</a>
        </div>
      </div>
    </div>
  </div>
  {% endfor %}
</div>
