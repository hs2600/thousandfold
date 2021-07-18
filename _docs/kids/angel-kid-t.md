---
title: Kids
permalink: /kids/tops/angel-kid-t/
---

<div>
    {% assign products = site.data.products | where:"id","19" %}

    {% for product in products %}

        {% include product.html %}

    {% endfor %}

</div>

***