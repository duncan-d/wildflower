---
layout: default
title: Stylists
---
<div class="row">
  {% assign stylists = site.stylists | sort: 'last_name' | reverse | sort: 'position' %}
  {% for stylist in stylists %}
  <!-- Card for small screens/phones -->
  <div class="col mb-5 d-sm-none">
    <a href="{{ site.baseurl }}{{ stylist.url }}">
      <div style="width: 10rem;" class="card bg-primary mx-auto">
        <img style="min-height: 80px" class="card-img" src="{{ site.baseurl }}/assets/images/{{ stylist.image_link | default: "blank_image.png" }}" alt="{{ stylist.name }}">
        <div class="card-img-overlay h-100 d-flex flex-column justify-content-end">
          <div class="card-text text-danger">
            <h5 class="bg-primary text-black border-secondary rounded p-1 m-0 text-center">{{ stylist.first_name }} {{ stylist.last_name }}</h5>
          </div>
        </div>
      </div>
    </a>
  </div>
  <!-- card for larger screens -->
  <div class="col mb-3 mx-1 d-none d-sm-inline">
    <div style="width: 15rem;" class="card bg-primary mx-auto">
      <a href="{{ site.baseurl }}{{ stylist.url }}">
        <img style="" class="card-img-top" src="{{ site.baseurl }}/assets/images/{{ stylist.image_link  | default: "blank_image.png" }}" alt="{{ stylist.name }}">
      </a>
      <div class="card-body">
        <div class="card-text">
          <h5 class="bg-primary border-secondary rounded p-1 mb-2 text-center">{{ stylist.first_name }} {{ stylist.last_name }} - {{ stylist.position }}</h5>
          <a class="btn btn-dark w-100 text-center" href="mailto:{{ stylist.email | default: "wildflowersalonmpls@gmail.com" }}">Email</a>
          <a class="btn btn-dark mt-1 w-100 text-center" href="{{ stylist.custom_vagaro_link | default: site.vagaro_link }}">Book Now</a>
        </div>
      </div>
    </div>
  </div>
  {% endfor %}
</div>
<div class="row">
  <div class="col-12 text-center">
    <a href="/" class="btn btn-dark mt-2"><h3>&larr;</h3></a>
  </div>
</div>