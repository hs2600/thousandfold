---
title: Test
permalink: /shop/test/
layout: default
---

{% assign products = site.data.products | where:"available", "true" %}

<div class="container">
  <h2> Featured Items</h2>
  <p>&nbsp;</p>
  <div class="row">
  {% for product in products %}
        <div class="col-md-3 img-container" style="height: 300px; border: 0px solid #efefef;">
          <a href="{{ site.baseurl }}/{{ product.category }}/{{ product.subcategory }}/{{ product.title | downcase | replace: " ", "-" | replace: ":", "" }}/">
          <img src="{{ site.baseurl }}/img/{{ product.image }}" class="img-thumbnail">
          <button class="btn btn-white enabled middle">
          View
          </button>
          </a>
          <h4 class="product-titlex"> {{ product.title }}</h4>
          <hr>          
          <span class="price">${{ product.price }}</span>
          <p>&nbsp;</p>
        </div>
  {% endfor %}
    </div>
</div>  

