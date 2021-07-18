---
title: Tops & Tees
permalink: /women/tops/
---

{% assign products = site.data.products | where:"category","women" | where: "subcategory","tops" | where:"available", "true" %}

<div>
{% if products.size == 0 %}
    <h3>Coming soon...</h3>
{% endif %}
    <div class="row">
        {% for product in products %}
            <div class="col-md-4 img-container">
            <a href="{{ site.baseurl }}/{{ product.category }}/{{ product.subcategory }}/{{ product.title | downcase | replace: " ", "-" | replace: ":", "" }}/">
            <img src="{{ site.baseurl }}/img/{{ product.image }}" class="img-thumbnail" style="max-height: 195px;">
            <button class="btn btn-danger enabled middle">
            View
            </button>
            </a>
            <h2 class="product-titlex" style="font-size: 14px;"> {{ product.title }}</h2>
            <hr>
            <span class="price">${{ product.price }}</span><br><br>
            <p>&nbsp;</p>
            </div>
        {% endfor %}
    </div>
</div>    
