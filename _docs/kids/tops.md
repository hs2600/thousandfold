---
title: Tops & Tees
layout: docs-notitle
permalink: /kids/tops/
---

{% assign products = site.data.products | where:"category","kids" | where: "subcategory","tops" | where:"available", "true" %}

<div>
{% if products.size == 0 %}
    <h3>Coming soon...</h3>
{% endif %}
    <div class="row">
        {% for product in products %}
        <div class="col-md-4 img-container">
        <span class="featured" style="position: absolute; top:30px;left:30px;z-index: 1; opacity: 0.7">{{ product.tag }}</span>
        <a href="{{ site.baseurl }}/{{ product.category }}/{{ product.subcategory }}/{{ product.title | downcase | replace: " ", "-" | replace: ":", "" }}/">
        <img src="{{ site.baseurl }}/img/{{ product.image }}" class="img-thumbnail" style="max-height:175px">
        <span class="white-button middle" style="margin-bottom: 30px;">
        View
        </span>
        </a><br>
        <span class="price">${{ product.price }}</span><br>
        <span class="product-title" style="font-size: 14px;"> {{ product.title }}</span>
        <hr style="margin-top: 10px; margin-bottom: 20px">
        </div>
        {% endfor %}
    </div>
</div>    
