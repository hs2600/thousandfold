---
title: Hats
layout: docs-notitle
permalink: /men/hats/
---

{% assign products = site.data.products | where:"category","men" | where: "subcategory","hats" | where:"available", "true" %}

<div>
{% if products.size == 0 %}
    <h3>Coming soon...</h3>
{% endif %}
    <div class="row">
        {% for product in products %}
            <div class="col-md-4 img-container">
            <a href="{{ site.baseurl }}/{{ product.category }}/{{ product.subcategory }}/{{ product.title | downcase | replace: " ", "-" | replace: ":", "" }}/">
            <img src="{{ site.baseurl }}/img/{{ product.image }}" class="img-thumbnail" style="max-height: 195px;">
            <button class="btn btn-success enabled middle">
            View
            </button>
            </a>
            <h2 class="product-titlex" style="font-size: 14px;"> {{ product.title }}</h2>
            <hr>
            <span class="price">${{ product.price }}</span><br><br>
            </div>
        {% endfor %}
    </div>
</div>    