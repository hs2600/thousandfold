---
title: Men
permalink: /men/hoodies/victory-hoodie/
---

<div>
    {% assign products = site.data.products | where:"id","6" %}

    {% for product in products %}

        {% include product.html %}

    {% endfor %}

</div>

***