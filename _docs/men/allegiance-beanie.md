---
title: Men
permalink: /men/hats/allegiance-beanie/
---

<div>
    {% assign products = site.data.products | where:"id","4" %}

    {% for product in products %}

        {% include product.html %}

    {% endfor %}

</div>

***