---
title: Men
permalink: /men/hats/suede-crown/
---

<div>
    {% assign products = site.data.products | where:"id","2" %}

    {% for product in products %}

        {% include product.html %}

    {% endfor %}

</div>

***