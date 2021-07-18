---
title: Women
permalink: /women/
layout: docs-notitle
---

![women]({{ site.baseurl }}/img/IMG_06052s.jpg "Women")

{% assign hats = site.data.products | where:"category","women" | where: "subcategory","hats" | where:"available", "true" %}
{% assign tops = site.data.products | where:"category","women" | where: "subcategory","tops" | where:"available", "true" %}
{% assign hoodies = site.data.products | where:"category","women" | where: "subcategory","hoodies" | where:"available", "true" %}

<div>
    <p>&nbsp;</p>
    <ul class="nav nav-pills" style="border-bottom: 3px solid #efefef;">
        <li class="#"><a href="#hats" data-toggle="tab">HATS</a></li>
        <li class="active"><a href="#tops" data-toggle="tab">TOPS</a></li>
        <li class="#"><a href="#hoodies" data-toggle="tab">HOODIES</a></li>
    </ul>
    <div id="myTabContent" class="tab-content" style="border: 0px solid #efefef; padding-top: 10px;">
        <div class="tab-pane fade" id="hats">
            <div class="row">
                {% for product in hats limit:8 %}
                    <div class="col-md-3 img-container">
                    <a href="{{ site.baseurl }}/{{ product.category }}/{{ product.subcategory }}/{{ product.title | downcase | replace: " ", "-" | replace: ":", "" }}/">
                    <img src="{{ site.baseurl }}/img/{{ product.image }}" class="img-thumbnail">
                    <span class="white-button middle" style="margin-bottom: 30px;">
                    View
                    </span>
                    </a>
                    <h2 class="product-titlex" style="font-size: 14px;"> {{ product.title }}</h2>
                    <hr>
                    <span class="featured">{{ product.tag }}</span>
                    <span class="price">${{ product.price }}</span><br><br>
                    </div>
                {% endfor %}
            </div>
        </div>
        <div class="tab-pane fade active in" id="tops">
            <div class="row">
                {% for product in tops limit:8 %}
                    <div class="col-md-3 img-container">
                    <a href="{{ site.baseurl }}/{{ product.category }}/{{ product.subcategory }}/{{ product.title | downcase | replace: " ", "-" | replace: ":", "" }}/">
                    <img src="{{ site.baseurl }}/img/{{ product.image }}" class="img-thumbnail">
                    <span class="white-button middle" style="margin-bottom: 30px;">
                    View
                    </span>
                    </a>
                    <h2 class="product-titlex" style="font-size: 14px;"> {{ product.title }}</h2>
                    <hr>
                    <span class="featured">{{ product.tag }}</span>
                    <span class="price">${{ product.price }}</span><br><br>
                    </div>
                {% endfor %}
            </div>
        </div>
        <div class="tab-pane fade" id="hoodies">
            <div class="row">
                {% for product in hoodies limit:8 %}
                    <div class="col-md-3 img-container">
                    <a href="{{ site.baseurl }}/{{ product.category }}/{{ product.subcategory }}/{{ product.title | downcase | replace: " ", "-" | replace: ":", "" }}/">
                    <img src="{{ site.baseurl }}/img/{{ product.image }}" class="img-thumbnail">
                    <span class="white-button middle" style="margin-bottom: 30px;">
                    View
                    </span>
                    </a>
                    <h2 class="product-titlex" style="font-size: 14px;"> {{ product.title }}</h2>
                    <hr>
                    <span class="featured">{{ product.tag }}</span>
                    <span class="price">${{ product.price }}</span><br><br>
                    </div>
                {% endfor %}
            </div>
        </div>        
    </div>
</div>    

