README
======

Installation
------------

Install using Composer:

```
./composer require evercodelab/banner-bundle
```

Add the bundle to your AppKernel.php:

``` php
$bundles = array(
    //...
    new Evercode\Bundle\BannerBundle\EvercodeBannerBundle(),
);
```

Add it to your routing.yml:

```
EvercodeBannerBundle:
    resource: "@EvercodeBannerBundle/Controller/"
    type:     annotation
```

In your templates, add:

```
{% render 'EvercodeBannerBundle:Banner:view' with {'place': 'Main_horizontal'} %}
```

You can optionally specify an assetic filter to automatically resize and/or compress your images:

```
{% render 'EvercodeBannerBundle:Banner:view' with {'place': 'Main_horizontal', 'filter': 'banner_main_horizontal'} %}
```

TODO: Define Assetic filter in config.yml
