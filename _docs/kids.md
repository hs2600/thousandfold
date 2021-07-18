---
title: Kids
permalink: /kids/
layout: docs-notitle
---

![kids]({{ site.baseurl }}/img/IMG_14082.jpg "Kids")

{% assign tops = site.data.products | where:"category","kids" | where: "subcategory","tops" | where:"available", "true" %}

<div>
    <p>&nbsp;</p>
    <ul class="nav nav-pills" style="border-bottom: 3px solid #efefef;">
        <li class="#"><a href="#tops" data-toggle="tab">TOPS</a></li>
    </ul>
    <div id="myTabContent" class="tab-content" style="border: 0px solid #efefef; padding-top: 10px;">
        <div class="tab-pane fade active in" id="tops">
            <div class="row">
                {% for product in tops limit:4 %}
                    <div class="col-md-3 img-container">
                    <a href="{{ site.baseurl }}/{{ product.category }}/{{ product.subcategory }}/{{ product.title | downcase | replace: " ", "-" | replace: ":", "" }}/">
                    <img src="{{ site.baseurl }}/img/{{ product.image }}" class="img-thumbnail">
                    <span class="white-button middle" style="margin-bottom: 30px;">
                    View
                    </span>
                    </a>
                    <h2 class="product-title" style="font-size: 14px;"> {{ product.title }}</h2>
                    <hr>
                    <span class="featured">{{ product.tag }}</span>
                    <span class="price">${{ product.price }}</span>
                    </div>
                {% endfor %}
            </div>
        </div>
    </div>
</div>   
