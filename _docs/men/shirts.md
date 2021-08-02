---
title: Shirts
layout: docs-notitle
permalink: /men/shirts/
---

{% assign products = site.data.products | where:"category","men" | where: "subcategory","shirts" | where:"available", "true" %}

<div>
{% if products.size == 0 %}
    <h3>Coming soon...</h3>
{% endif %}
    <div class="row">
        {% for product in products %}
        <div class="col-md-4 img-container">
        <span class="featured" style="position: absolute; top:30px;left:30px;z-index: 1; opacity: 0.7">{{ product.tag }}</span>
        <a href="{{ site.baseurl }}/{{ product.category }}/{{ product.subcategory }}/{{ product.title | downcase | replace: " ", "-" | replace: ":", "" }}/">
        <img src="{{ site.baseurl }}/img/{{ product.image }}" class="img-thumbnail" style="width: 100%;">
        <span class="white-button middle" style="margin-bottom: 30px;">
        View
        </span>
        </a><br>
        <span class="price">${{ product.price }}</span><br>
        <span class="product-title" style="font-size: 14px;"> {{ product.title }}</span>
        {% for colorx in product.colors %}
            {% if colorx == "Burgundy" %}
                {% assign color = "#800020" %}
            {% elsif colorx == "Heather Dark Gray" %}
                {% assign color = "#353638" %}
            {% elsif colorx == "Heather Gray" %}
                {% assign color = "#767691" %}
            {% elsif colorx == "Heather Blue" %}
                {% assign color = "#667CDB" %}
            {% elsif colorx == "Pop Blue" %}
                {% assign color = "#7AB4F1" %}
            {% elsif colorx == "Rustic Green" %}
                {% assign color = "#61969C" %}
            {% elsif colorx == "Vibrant Red" %}
                {% assign color = "#DD2229" %}
            {% elsif colorx == "Soft Pink" %}
                {% assign color = "#EFBFD8" %}                
            {% else %}
                {% assign color = colorx %}
            {% endif %}
            {% if color contains "/" %}
                {% assign colors = color | split: "/" %}
                <span class="dot_split" style="background: linear-gradient(
                    to right, 
                    {% for color in colors limit:1 %}            
                    {{ color }} 0%,
                    {{ color }} 50%,
                    {% endfor %}
                    {% for color in colors offset:1 %}            
                    {{ color }} 50%,
                    {{ color }} 100%
                    {% endfor %}            
                );">
                </span>
            {% else %}
                <span class="dot" style="background-color: {{ color }}"></span>
            {% endif %}
        {% endfor %}           
        <hr style="margin-top: 10px; margin-bottom: 20px">
        </div>
        {% endfor %}
    </div>
</div>    
