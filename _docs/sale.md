---
title: Sale
permalink: /sale/
layout: docs-nonav
---
<style>

.header-container{
  background: url('../../img/BeFunky-collage.jpg') no-repeat 100% 70%;
  background-attachment: fixed;
  background-size: 100%;
  height: 400px;
}

</style>

<br>

<div class="header-container">
</div>
<br>

{% assign products = site.data.products | where:"available", "true" | where:"tag", "Sale" | sort:"product.id" | reverse %}

<div class="row" style="padding: 15px">
    {% for product in products %}

        {% include product_preview.html %}

    {% endfor %}
</div>

  
