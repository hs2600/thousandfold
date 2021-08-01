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
                    <div class="col-md-3 img-container" style="margin: 0px; width: 200px; height:250px;">
                    <span class="featured" style="position: absolute; top:30px;left:30px;z-index: 1; opacity: 0.7">{{ product.tag }}</span>
                    <a href="{{ site.baseurl }}/{{ product.category }}/{{ product.subcategory }}/{{ product.title | downcase | replace: " ", "-" | replace: ":", "" }}/">
                    <img src="{{ site.baseurl }}/img/{{ product.image }}" class="img-thumbnail" style="max-height:175px">
                    <span class="white-button middle" style="margin-bottom: 30px;">
                    View
                    </span>
                    </a>
                    <span class="price">${{ product.price }}</span><br>
                    <span class="product-title" style="font-size: 14px;"> {{ product.title }}</span>
                    <hr style="margin-top: 10px; margin-bottom: 20px">
                    </div>
                {% endfor %}
            </div>
        </div>
    </div>
</div>   
