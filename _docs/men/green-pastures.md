---
title: Men
permalink: /men/hoodies/green-pastures/
---

<div>
    {% assign products = site.data.products | where:"id","24" %}

    {% for product in products %}

        {% include product.html %}

    {% endfor %}

</div>

***
