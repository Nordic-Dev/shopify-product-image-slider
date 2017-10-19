# Image carousel for Shopify product images
There are a lot of out of the box apps for sliders on the Shopify App market but I wasn't able to get one that just took the product images and wrapped them in a simple slider. This implementation uses Slick  

## Implementation of the [Slick image carousel](http://kenwheeler.github.io/slick/) by [@kenwheeler](https://github.com/kenwheeler/slick/) into a Shopify store.

### Reference the Slick css and js files in your theme.liquid file. 

```
  <link rel="stylesheet" type="text/css" href="https://cdnjs.cloudflare.com/ajax/libs/slick-carousel/1.8.1/slick.min.css"/>
  <link rel="stylesheet" type="text/css" href="https://cdnjs.cloudflare.com/ajax/libs/slick-carousel/1.8.1/slick-theme.min.css"/>
  <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/slick-carousel/1.8.1/slick.min.js"></script>
```

### Create new file called product-image-slider.liquid
In your Shopify theme, create a new snippet called product-image-slider.liquid

### Reference the new product-image-slider.liquid from your product template
From your product page template(product-template.liquid) remove the contents from ```<section class="primary-images">``` and paste the include statement to the product-image-slider.liquid file. 

```
<section class="primary-images">
    {% include 'product-image-slider' %}
</section>
```

*Not all Shopify themes are the same so yours might not have a product-template.liquid file in the sections folder. If that's the case look around for your product page template and insert this new code into that template file.
