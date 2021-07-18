---
title: Shop
permalink: /shop/
layout: default
---

<style>

.header-container{
  background: url('../img/lhwmOvY4.jpeg') no-repeat 0 0%;
  background-size: 100%;
  background-attachment: fixed;
  max-height: 300px;
  color: #FFF;
}

</style>

<div class="header-container jumbotron">
  <div class="container">
    <h1>Our Products</h1>
    <p>&nbsp;</p>
  </div>
</div>

<div class="d-none d-lg-block" style="height:40px"></div>
<div style="height:40px"></div>

<div class="container">
  <div class="row" style="border: 0px solid red; padding: 15px;">
    <div class="col-md-4 img-container" style="padding: 0px;">
      <a href="/men/">
      <img src="{{ site.baseurl }}/img/men.jpg" width="100%" class="img-preview">
      <span class="middle-vis" style="background-color: white; color: black; width: 150px; padding: 8px; text-align: center; border-radius: 2px; border-bottom: 3px solid gray">
      Men <span class="fa fa-arrow-circle-right"></span>
      </span>
      </a>              
    </div>
    <div class="col-md-4 img-container" style="padding: 0px;">
      <a href="/women/">
      <img src="{{ site.baseurl }}/img/women.jpg" width="100%" class="img-preview">
      <span class="middle-vis" style="background-color: white; color: black; width: 150px; padding: 8px; text-align: center; border-radius: 2px; border-bottom: 3px solid gray">
      Women <span class="fa fa-arrow-circle-right"></span>
      </span>
      </a>   
    </div>
    <div class="col-md-4 img-container" style="padding: 0px;">
      <a href="/kids/">
      <img src="{{ site.baseurl }}/img/kids.jpg" width="100%" class="img-preview">
      <span class="middle-vis" style="background-color: white; color: black; width: 150px; padding: 8px; text-align: center; border-radius: 2px; border-bottom: 3px solid gray">
      Kids <span class="fa fa-arrow-circle-right"></span>
      </span>
      </a>   
    </div>        
  </div>

  {% assign men = site.data.products | where:"category","men" | where_exp:"product","product.tag == 'Sale' or product.tag == 'Featured'" | where:"available", "true" | sort:"product.id" | reverse %}
  {% assign women = site.data.products | where:"category","women" | where_exp:"product","product.tag == 'Sale' or product.tag == 'Featured'" | where:"available", "true" | sort:"product.id" | reverse %}
  {% assign kids = site.data.products | where:"category","kids" | where_exp:"product","product.tag == 'Sale' or product.tag == 'Featured'" | where:"available", "true" | sort:"product.id" | reverse %}

  <div>
    <p>&nbsp;</p>
    <h1>Featured Items</h1>
    <ul class="nav nav-pills" style="border-bottom: 3px solid #efefef;">    
      <li class="active"><a href="#men" data-toggle="tab">MEN</a></li>
      <li class="#"><a href="#women" data-toggle="tab">WOMEN</a></li>
      {% if kids.size > 0 %}
      <li class="#"><a href="#kids" data-toggle="tab">KIDS</a></li>
      {% endif %}
    </ul>
    <div id="myTabContent" class="tab-content" style="border: 0px solid #efefef; padding: 15px; padding-top: 5px;">
      <div class="tab-pane fade active in" id="men">
        <div class="row">
          {% for product in men limit:6 %}
            <div class="col-md-4 img-container" style="padding: 0px;">
            <a href="{{ site.baseurl }}/{{ product.category }}/{{ product.subcategory }}/{{ product.title | downcase | replace: " ", "-" | replace: ":", "" }}/">
            <img src="{{ site.baseurl }}/img/{{ product.image }}" class="img-preview" style="width: 100%;max-height: 250px;">
            <span class="white-button middle" style="margin-bottom: 30px;">
            View
            </span>
            </a>
            <h2 class="product-titlex" style="font-size: 14px;"> {{ product.title }}</h2>
            <hr style="width: 95%">
            <span class="featured">{{ product.tag }}</span>
            <span class="price">${{ product.price }}</span><br><br>
            </div>
          {% endfor %}
        </div>
      </div>
      <div class="tab-pane fade" id="women">
        <div class="row">
          {% for product in women limit:6 %}
            <div class="col-md-4 img-container" style="padding: 0px;">
            <a href="{{ site.baseurl }}/{{ product.category }}/{{ product.subcategory }}/{{ product.title | downcase | replace: " ", "-" | replace: ":", "" }}/">
            <img src="{{ site.baseurl }}/img/{{ product.image }}" class="img-preview" style="width: 100%;max-height: 250px;">
            <span class="white-button middle" style="margin-bottom: 30px;">
            View
            </span>
            </a>
            <h2 class="product-titlex" style="font-size: 14px;"> {{ product.title }}</h2>
            <hr style="width: 95%">
            <span class="featured">{{ product.tag }}</span>
            <span class="price">${{ product.price }}</span><br><br>
            </div>
          {% endfor %}
        </div>
      </div>
      <div class="tab-pane fade" id="kids">
        <div class="row">
          {% for product in kids limit:4 %}
            <div class="col-md-4 img-container" style="padding: 0px;">
            <a href="{{ site.baseurl }}/{{ product.category }}/{{ product.subcategory }}/{{ product.title | downcase | replace: " ", "-" | replace: ":", "" }}/">
            <img src="{{ site.baseurl }}/img/{{ product.image }}" class="img-preview" style="width: 100%;">
            <span class="white-button middle" style="margin-bottom: 30px;">
            View
            </span>
            </a>
            <h2 class="product-titlex" style="font-size: 14px;"> {{ product.title }}</h2>
            <hr style="width: 95%">
            <span class="featured">{{ product.tag }}</span>
            <span class="price">${{ product.price }}</span><br><br>
            </div>
          {% endfor %}
        </div>
      </div>    
    </div>

<hr>
  <div style="padding: 0px;">
    <div class="row" style="padding: 15px;">
      <div class="col-sm-6 col-md-6 col-lg-6" style="padding: 0px;">
        <img src="{{ site.baseurl }}/img/IMG_6159.jpg" width="100%">
      </div>        
      <div class="col-sm-6 col-md-6 col-lg-6" style="padding: 0px;">
        <img src="{{ site.baseurl }}/img/IMG_4916.jpg" width="100%">
      </div>        
    </div>
  </div>

  </div>
</div>  

