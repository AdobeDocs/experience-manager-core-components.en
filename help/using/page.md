---
title: Page Component
seo-title: Page Component
description: The Page Component is an extensible page component designed to work with the template editor and allow page header/footer and structure components to be assembled with the template editor.
seo-description: The Page Component is an extensible page component designed to work with the template editor and allow page header/footer and structure components to be assembled with the template editor.
uuid: 7052a5b1-e7f1-4944-a55c-faf739b6e89c
contentOwner: User
content-type: reference
topic-tags: authoring
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: cb1a745a-30c4-4ad6-a04f-fefb3666cd95
---

# Page Component{#page-component}

The Page Component is an extensible page component designed to work with the [template editor](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/templates.html) and allows page header/footer and structure components to be assembled with the template editor.

## Usage {#usage}

The page component forms the basis of all pages designed with the core components as well as editable templates. By using the page component, headers, footers, and the structure of the page can be defined as a template using the other core components.

Using the [design dialog](page.md#main-pars_title_1995166862), custom client-side libraries can be defined for the page. Unlike other components which have an edit dialog accessible directly from the component, because the component is the page itself, the [edit dialog](page.md#main-pars_title) of the page component is the page properties window.

## Version and Compatibility {#version-and-compatibility}

The current version of the Page Component is v2, which was introduced with release 2.0.0 of the Core Components in January 2018, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.3|AEM 6.4|
|-|-|-|
|v2|Compatible|Compatible|
|[v1](page-v1.md)|Compatible|Compatible|

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

>[!NOTE]
>
>To enable redirect at `cq:Page` level for verison 2 of the page component and AEM 6.3, [service pack 2](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp2-release-notes.html) or later is required. Such redirection was not available in prior releases.

## Sample Component Output {#sample-component-output}

The following is sample taken from [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

![](assets/chlimage_1.png) 

### HTML {#html}

```
<!DOCTYPE HTML>
<html lang="en">
    <head>
    <meta charset="UTF-8">
    <title>Equipment</title>
        <meta name="template" content="hero-page"/>
    
<link rel="stylesheet" href="/etc.clientlibs/weretail/clientlibs/clientlib-dependencies.css" type="text/css">
<script type="text/javascript" src="/etc.clientlibs/weretail/clientlibs/clientlib-dependencies.js"></script>

<link rel="stylesheet" href="/etc.clientlibs/clientlibs/granite/jquery-ui.css" type="text/css">
<link rel="stylesheet" href="/etc.clientlibs/weretail/clientlibs/clientlib-base.css" type="text/css">

<script src="https://use.typekit.net/dje4ayd.js"></script>
<script>try {
    Typekit.load({async: true});
} catch (e) {
}</script>

<script type="text/javascript">
            (function() {
                window.ContextHub = window.ContextHub || {};

                /* setting paths */
                ContextHub.Paths = ContextHub.Paths || {};
                ContextHub.Paths.CONTEXTHUB_PATH = "/libs/settings/cloudsettings/legacy/contexthub";
                ContextHub.Paths.RESOURCE_PATH = "\/content\/we\u002Dretail\/us\/en\/equipment\/_jcr_content\/contexthub";
                ContextHub.Paths.SEGMENTATION_PATH = "\/conf\/we\u002Dretail\/settings\/wcm\/segments";
                ContextHub.Paths.CQ_CONTEXT_PATH = "";

                /* setting initial constants */
                ContextHub.Constants = ContextHub.Constants || {};
                ContextHub.Constants.ANONYMOUS_HOME = "/home/users/5/5pg2H1cbhOdmdhAhFib6";
                ContextHub.Constants.MODE = "no-ui";
            }());
        </script><script src="/etc/cloudsettings.kernel.js/libs/settings/cloudsettings/legacy/contexthub" type="text/javascript"></script>

</head>
    <body class="page">

<div class="container">
    <div class="root responsivegrid">

<div class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
    
    <div class="header aem-GridColumn aem-GridColumn--default--12">

    <div class="we-retail-header" data-we-header-content="/content/we-retail/us/en/equipment.header_include.html">
        
<div class="we-SearchModal modal fade" id="navbar-search" role="dialog" data-color="primary">
    <div class="modal-dialog">
        <div class="modal-content">
            <div class="modal-header">
                <span><i class="we-Icon we-Icon--search"></i>Search anything</span>
                <button type="button" class="close" data-dismiss="modal"><span>Close search</span><i class="we-Icon we-Icon--close-alt"></i>
                </button>
            </div>
            <div class="modal-body">
                <div class="row">
                    <div class="col-md-12">
                        <form id="form-search-input-inline" data-paths="[/content/we-retail/us/en]" class="scf-js-searchform navbar-form navbar-left" role="search">
                            <div class="scf-quicksearch-form-group form-group">
                                <input type="search" id="scf-js-quicksearch-input-inline" placeholder="Start typing..." data-dropdown="drop_search" aria-controls="drop_search" aria-expanded="false" name="input_value" class="we-SearchModal-input" value="" required="" autocomplete="off">
                                <span role="status" aria-live="polite" class="ui-helper-hidden-accessible"></span>
                                <input type="hidden" name="resultPage" class="scf-js-seach-resultPage" value="/content/we-retail/us/en/community/search"/>
                                <input type="hidden" name="searchEndpoint" class="scf-js-search-endpoint" value="/content/we-retail/us/en/community/search/jcr:content/content/primary/searchresult"/>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
<!-- /.we-SearchModal -->

<div class="we-LanguageModal modal fade" tabindex="-1" role="dialog" data-color="primary">
    <div class="modal-dialog modal-center modal-sm">
        <div class="modal-content">
            <div class="modal-header">
                <h3 class="modal-title text-center">CHOOSE YOUR COUNTRY</h3>
            </div>
            <div class="modal-body">
                <ul class="we-LanguagesList">
                    <li>
                        <i class="we-lang-icon we-lang-icon-us"></i><span><a href="/content/we-retail/us/en.html" class="active">English</a> |
                    <a href="/content/we-retail/us/es.html">Español</a></span>
                    </li>
                
                    <li>
                        <i class="we-lang-icon we-lang-icon-ca"></i><span><a href="/content/we-retail/ca/en.html">English</a> |
                    <a href="/content/we-retail/ca/fr.html">Français</a></span>
                    </li>
                
                    <li>
                        <i class="we-lang-icon we-lang-icon-ch"></i><span><a href="/content/we-retail/ch/de.html">Deutsch</a> |
                    <a href="/content/we-retail/ch/fr.html">Français</a> |
                    <a href="/content/we-retail/ch/it.html">Italiano</a></span>
                    </li>
                
                    <li>
                        <i class="we-lang-icon we-lang-icon-de"></i><span><a href="/content/we-retail/de/de.html">Deutsch</a></span>
                    </li>
                
                    <li>
                        <i class="we-lang-icon we-lang-icon-fr"></i><span><a href="/content/we-retail/fr/fr.html">Français</a></span>
                    </li>
                
                    <li>
                        <i class="we-lang-icon we-lang-icon-es"></i><span><a href="/content/we-retail/es/es.html">Español</a></span>
                    </li>
                
                    <li>
                        <i class="we-lang-icon we-lang-icon-it"></i><span><a href="/content/we-retail/it/it.html">Italiano</a></span>
                    </li>
                </ul>
            </div>
        </div>
        <div class="modal-after">
            <a href="#" data-dismiss="modal"><i class="we-Icon we-Icon--close-alt"></i> Close</a>
        </div>
    </div>
</div><!-- /.we-LanguageModal -->
    </div>
</div>
<div class="heroimage cmp-image aem-GridColumn aem-GridColumn--default--12">

    <div class="we-HeroImage width-full jumbotron" style="background-image: url('/content/we-retail/us/en/equipment/jcr%3acontent/root/hero_image.img.jpeg/1473680813224.jpeg');">
        <div class="container cq-dd-image">
            <div class="we-HeroImage-wrapper">
                <p class="h3"></p>
                <strong class="we-HeroImage-title h1">Equipment</strong>

            </div>
        </div>
    </div>

</div>
<div class="responsivegrid aem-GridColumn aem-GridColumn--default--12">

<div class="aem-Grid aem-Grid--12 aem-Grid--default--12 ">
    
    <div class="title aem-GridColumn aem-GridColumn--default--12">
<div class="cmp-title">
    <h2 class="cmp-title__text">Welcome this is our finest equipment</h2>
</div>

</div>
<div class="categoryteaser image aem-GridColumn--default--none aem-GridColumn aem-GridColumn--default--6 aem-GridColumn--offset--default--0">
<div class="we-CategoryTeaser">
    <div class="crop crop-16_9 cmp cmp-image">
<div class="cmp-image">

            <img class="cmp-image__image" src="/content/we-retail/us/en/equipment/_jcr_content/root/responsivegrid/category_teaser.img.jpeg/1473680823274.jpeg" alt="Hiker on the trek in Himalayas, Anapurna valley, Nepal" title="Hiker Anapurna"/>

</div>

</div>

    <h2></h2>
    <h3></h3>
    
    <a href="/content/we-retail/us/en/products/equipment/hiking.html" class="btn btn-action btn-primary">Hiking</a>
</div>
</div>
<div class="categoryteaser image aem-GridColumn--default--none aem-GridColumn aem-GridColumn--default--6 aem-GridColumn--offset--default--0">
<div class="we-CategoryTeaser">
    <div class="crop crop-16_9 cmp cmp-image">
<div class="cmp-image">

            <img class="cmp-image__image" src="/content/we-retail/us/en/equipment/_jcr_content/root/responsivegrid/category_teaser_2082536754.img.jpeg/1473680831529.jpeg" alt="Trail running man exercising outdoors for fitness" title="Running Trail Man"/>

</div>

</div>

    <h2></h2>
    <h3></h3>
    
    <a href="/content/we-retail/us/en/products/equipment/running.html" class="btn btn-action btn-primary">Running</a>
</div>
</div>
<div class="categoryteaser image aem-GridColumn--default--none aem-GridColumn aem-GridColumn--offset--default--0 aem-GridColumn--default--4">
<div class="we-CategoryTeaser">
    <div class="crop crop-16_9 cmp cmp-image">
<div class="cmp-image">

            <img class="cmp-image__image" src="/content/we-retail/us/en/equipment/_jcr_content/root/responsivegrid/category_teaser_647414391.img.jpeg/1473680769375.jpeg" alt="Enduro mountain biking in the forest" title="Enduro Trail Jump"/>

</div>

</div>

    <h2></h2>
    <h3></h3>
    
    <a href="/content/we-retail/us/en/products/equipment/biking.html" class="btn btn-action btn-primary">Biking</a>
</div>
</div>
<div class="categoryteaser image aem-GridColumn--default--none aem-GridColumn aem-GridColumn--offset--default--0 aem-GridColumn--default--4">
<div class="we-CategoryTeaser">
    <div class="crop crop-16_9 cmp cmp-image">
<div class="cmp-image">

            <img class="cmp-image__image" src="/content/we-retail/us/en/equipment/_jcr_content/root/responsivegrid/category_teaser_1341949589.img.jpeg/1473680798215.jpeg" alt="Surfing in Nicaragua" title="Wave Nicaragua"/>

</div>

</div>

    <h2></h2>
    <h3></h3>
    
    <a href="/content/we-retail/us/en/products/equipment/surfing.html" class="btn btn-action btn-primary">Surfing</a>
</div>
</div>
<div class="categoryteaser image aem-GridColumn--default--none aem-GridColumn aem-GridColumn--offset--default--0 aem-GridColumn--default--4">
<div class="we-CategoryTeaser">
    <div class="crop crop-16_9 cmp cmp-image">
<div class="cmp-image">

            <img class="cmp-image__image" src="/content/we-retail/us/en/equipment/_jcr_content/root/responsivegrid/category_teaser_1398042708.img.jpeg/1473680831357.jpeg" alt="Steep skiing above valley" title="Freeride Steep"/>

</div>

</div>

    <h2></h2>
    <h3></h3>
    
    <a href="/content/we-retail/us/en/products/equipment/snow-sports.html" class="btn btn-action btn-primary">Snow Sports</a>
</div>
</div>
<div class="title aem-GridColumn aem-GridColumn--default--12">
<div class="cmp-title">
    <h2 class="cmp-title__text">Featured products</h2>
</div>

</div>
<div class="productgrid list aem-GridColumn aem-GridColumn--default--12">
<div class="we-product-grid-container">
    <ul class="foundation-ordered-list-container">
        
<li class="foundation-list-item">
    <we-product-item price="$110.00" size="11,12,7,8,9,10" inline-template>
        <div class="we-ProductsGrid-item">
            <div class="we-ProductsGrid-item-image img-center">
                <div class="image">
<div class="cmp-image">

            <img class="cmp-image__image" src="/content/we-retail/us/en/products/equipment/biking/marin-mountain-bike-shoes/_jcr_content/root/product/image.img.jpeg/1473680884256.jpeg" alt/>

</div>

</div>

            </div>

            <h3 class="we-ProductsGrid-item-title h4">Marin Mountain Bike Shoes</h3>
            <span class="we-ProductsGrid-item-subtitle small text-muted">footwear</span>

            <strong class="we-ProductsGrid-item-price">
                <span>$110.00</span>
                <span class="we-ProductsGrid-item-price-new"></span>
                <s class="we-ProductsGrid-item-price-old"></s>
            </strong>

            <span class="we-ProductsGrid-item-discount hidden"><span></span>off</span>
            <a href="/content/we-retail/us/en/products/equipment/biking/marin-mountain-bike-shoes.html" class="we-ProductsGrid-item-link"></a>

        </div>
        <!-- /.we-ProductsGrid-item -->
    </we-product-item>
</li>

<li class="foundation-list-item">
    <we-product-item price="$65.00" size="11,13,9" inline-template>
        <div class="we-ProductsGrid-item">
            <div class="we-ProductsGrid-item-image img-center">
                <div class="image">
<div class="cmp-image">

            <img class="cmp-image__image" src="/content/we-retail/us/en/products/equipment/running/fleet-cross-training-shoe/_jcr_content/root/product/image.img.jpeg/1473680885053.jpeg" alt/>

</div>

</div>

            </div>

            <h3 class="we-ProductsGrid-item-title h4">Fleet Cross-Training Shoe</h3>
            <span class="we-ProductsGrid-item-subtitle small text-muted">footwear</span>

            <strong class="we-ProductsGrid-item-price">
                <span>$65.00</span>
                <span class="we-ProductsGrid-item-price-new"></span>
                <s class="we-ProductsGrid-item-price-old"></s>
            </strong>

            <span class="we-ProductsGrid-item-discount hidden"><span></span>off</span>
            <a href="/content/we-retail/us/en/products/equipment/running/fleet-cross-training-shoe.html" class="we-ProductsGrid-item-link"></a>

        </div>
        <!-- /.we-ProductsGrid-item -->
    </we-product-item>
</li>

<li class="foundation-list-item">
    <we-product-item price="$75.00" size="S,XL,L,M" inline-template>
        <div class="we-ProductsGrid-item">
            <div class="we-ProductsGrid-item-image img-center">
                <div class="image">
<div class="cmp-image">

            <img class="cmp-image__image" src="/content/we-retail/us/en/products/equipment/biking/sequoia-bike-helmet/_jcr_content/root/product/image.img.jpeg/1473680800543.jpeg" alt/>

</div>

</div>

            </div>

            <h3 class="we-ProductsGrid-item-title h4">Sequoia Bike Helmet</h3>
            <span class="we-ProductsGrid-item-subtitle small text-muted">helmet</span>

            <strong class="we-ProductsGrid-item-price">
                <span>$75.00</span>
                <span class="we-ProductsGrid-item-price-new"></span>
                <s class="we-ProductsGrid-item-price-old"></s>
            </strong>

            <span class="we-ProductsGrid-item-discount hidden"><span></span>off</span>
            <a href="/content/we-retail/us/en/products/equipment/biking/sequoia-bike-helmet.html" class="we-ProductsGrid-item-link"></a>

        </div>
        <!-- /.we-ProductsGrid-item -->
    </we-product-item>
</li>

<li class="foundation-list-item">
    <we-product-item price="$39.00" size="XXS,S,XL,L,M,XXL" inline-template>
        <div class="we-ProductsGrid-item">
            <div class="we-ProductsGrid-item-image img-center">
                <div class="image">
<div class="cmp-image">

            <img class="cmp-image__image" src="/content/we-retail/us/en/products/equipment/hiking/rios-t-shirt/_jcr_content/root/product/image.img.jpeg/1473680862774.jpeg" alt/>

</div>

</div>

            </div>

            <h3 class="we-ProductsGrid-item-title h4">Rios T Shirt</h3>
            <span class="we-ProductsGrid-item-subtitle small text-muted">shirt</span>

            <strong class="we-ProductsGrid-item-price">
                <span>$39.00</span>
                <span class="we-ProductsGrid-item-price-new"></span>
                <s class="we-ProductsGrid-item-price-old"></s>
            </strong>

            <span class="we-ProductsGrid-item-discount hidden"><span></span>off</span>
            <a href="/content/we-retail/us/en/products/equipment/hiking/rios-t-shirt.html" class="we-ProductsGrid-item-link"></a>

        </div>
        <!-- /.we-ProductsGrid-item -->
    </we-product-item>
</li>

<li class="foundation-list-item">
    <we-product-item price="$900.00" inline-template>
        <div class="we-ProductsGrid-item">
            <div class="we-ProductsGrid-item-image img-center">
                <div class="image">
<div class="cmp-image">

            <img class="cmp-image__image" src="/content/we-retail/us/en/products/equipment/surfing/the-stretch-longboard/_jcr_content/root/product/image.img.png/1473680863680.png" alt/>

</div>

</div>

            </div>

            <h3 class="we-ProductsGrid-item-title h4">The Stretch Longboard</h3>
            <span class="we-ProductsGrid-item-subtitle small text-muted">equipment</span>

            <strong class="we-ProductsGrid-item-price">
                <span>$900.00</span>
                <span class="we-ProductsGrid-item-price-new"></span>
                <s class="we-ProductsGrid-item-price-old"></s>
            </strong>

            <span class="we-ProductsGrid-item-discount hidden"><span></span>off</span>
            <a href="/content/we-retail/us/en/products/equipment/surfing/the-stretch-longboard.html" class="we-ProductsGrid-item-link"></a>

        </div>
        <!-- /.we-ProductsGrid-item -->
    </we-product-item>
</li>

<li class="foundation-list-item">
    <we-product-item price="$39.99" inline-template>
        <div class="we-ProductsGrid-item">
            <div class="we-ProductsGrid-item-image img-center">
                <div class="image">
<div class="cmp-image">

            <img class="cmp-image__image" src="/content/we-retail/us/en/products/equipment/running/faba-running-pants/_jcr_content/root/product/image.img.jpeg/1473680883335.jpeg" alt/>

</div>

</div>

            </div>

            <h3 class="we-ProductsGrid-item-title h4">Faba Running Pants</h3>
            <span class="we-ProductsGrid-item-subtitle small text-muted">pants</span>

            <strong class="we-ProductsGrid-item-price">
                <span>$39.99</span>
                <span class="we-ProductsGrid-item-price-new"></span>
                <s class="we-ProductsGrid-item-price-old"></s>
            </strong>

            <span class="we-ProductsGrid-item-discount hidden"><span></span>off</span>
            <a href="/content/we-retail/us/en/products/equipment/running/faba-running-pants.html" class="we-ProductsGrid-item-link"></a>

        </div>
        <!-- /.we-ProductsGrid-item -->
    </we-product-item>
</li>
    </ul>
</div>

</div>
<div class="button aem-GridColumn aem-GridColumn--default--12">
<a class="btn btn-primary btn-action cq-dd-linkTo " href="/content/we-retail/us/en/products/equipment.html" role="button">All equipment</a>
</div>
<div class="title aem-GridColumn aem-GridColumn--default--12">
<div class="cmp-title">
    <h2 class="cmp-title__text">Winter is coming, get ready</h2>
</div>

</div>
<div class="categoryteaser image aem-GridColumn--default--none aem-GridColumn aem-GridColumn--default--6 aem-GridColumn--offset--default--0">
<div class="we-CategoryTeaser">
    <div class="crop crop-16_9 cmp cmp-image">
<div class="cmp-image">

            <img class="cmp-image__image" src="/content/we-retail/us/en/equipment/_jcr_content/root/responsivegrid/category_teaser_643606949.img.jpeg/1473680763953.jpeg" alt="Aggressive powder skiing" title="Freeride Extreme"/>

</div>

</div>

    <h2></h2>
    <h3></h3>
    
    <a href="/content/we-retail/us/en/products/equipment/snow-sports.html" class="btn btn-action btn-primary">Snow Sports</a>
</div>
</div>
<div class="categoryteaser image aem-GridColumn--default--none aem-GridColumn aem-GridColumn--default--6 aem-GridColumn--offset--default--0">
<div class="we-CategoryTeaser">
    <div class="crop crop-16_9 cmp cmp-image">
<div class="cmp-image">

            <img class="cmp-image__image" src="/content/we-retail/us/en/equipment/_jcr_content/root/responsivegrid/category_teaser_883210151.img.jpeg/1473680828178.jpeg" alt="Skiing deep powder in Siberia" title="Freeride Siberia"/>

</div>

</div>

    <h2></h2>
    <h3></h3>
    
    <a href="/content/we-retail/us/en/products/equipment/snow-sports.html" class="btn btn-action btn-primary">Snowboarding</a>
</div>
</div>

</div></div>
<div class="search aem-GridColumn aem-GridColumn--default--12">
<section class="cmp-search" role="search" data-results-size="10" data-search-term-minimum-length="3">
    <form method="get" action="/conf/we-retail/settings/wcm/templates/hero-page/structure/_jcr_content/root/search.result.html" class="cmp-search__form" autocomplete="off">
        <div class="cmp-search__field">
            <i class="cmp-search__icon"></i>
            <span class="cmp-search__loading-indicator"></span>
            <input class="cmp-search__input" type="text" placeholder="Search" name="fulltext" role="combobox" aria-autocomplete="list" aria-haspopup="true" aria-invalid="false">
            <button class="cmp-search__clear">
                <i class="cmp-search__clear-icon"></i>
            </button>
        </div>
    </form>
    <div class="cmp-search__results" role="listbox" aria-multiselectable="false"></div>
</section></div>
<div class="footer aem-GridColumn aem-GridColumn--default--12">

    <footer class="we-Footer">
        <div class="container">

            <div class="row">

                <div class="col-md-4">
                    <div class="we-Logo we-Logo--big">
                        we.<strong>Retail</strong>
                    </div>
                </div>

                <div class="col-md-8 col-xs-12">
                    
                        <div class="col-lg-2 col-md-2 col-xs-3">
                            <div class="we-Footer-nav">
                                <h2 class="h4">
                                    <a href="/content/we-retail/us/en/experience.html">Experience</a>
                                </h2>
                            </div>
                        </div>
                    
                        <div class="col-lg-2 col-md-2 col-xs-3">
                            <div class="we-Footer-nav">
                                <h2 class="h4">
                                    <a href="/content/we-retail/us/en/men.html">Men</a>
                                </h2>
                            </div>
                        </div>
                    
                        <div class="col-lg-2 col-md-2 col-xs-3">
                            <div class="we-Footer-nav">
                                <h2 class="h4">
                                    <a href="/content/we-retail/us/en/women.html">Women</a>
                                </h2>
                            </div>
                        </div>
                    
                        <div class="col-lg-2 col-md-2 col-xs-3">
                            <div class="we-Footer-nav">
                                <h2 class="h4">
                                    <a href="/content/we-retail/us/en/equipment.html">Equipment</a>
                                </h2>
                            </div>
                        </div>
                    
                        <div class="col-lg-2 col-md-2 col-xs-3">
                            <div class="we-Footer-nav">
                                <h2 class="h4">
                                    <a href="/content/we-retail/us/en/about-us.html">About Us</a>
                                </h2>
                            </div>
                        </div>
                    
                        <div class="col-lg-2 col-md-2 col-xs-3">
                            <div class="we-Footer-nav">
                                <h2 class="h4">
                                    <a href="/content/we-retail/us/en/products.html">Products</a>
                                </h2>
                            </div>
                        </div>
                    
                        <div class="col-lg-2 col-md-2 col-xs-3">
                            <div class="we-Footer-nav">
                                <h2 class="h4">
                                    <a href="/content/we-retail/us/en/community.html">community</a>
                                </h2>
                            </div>
                        </div>
                    
                        <div class="col-lg-2 col-md-2 col-xs-3">
                            <div class="we-Footer-nav">
                                <h2 class="h4">
                                    <a href="/content/we-retail/us/en/my-equipment.html">Equipment</a>
                                </h2>
                            </div>
                        </div>
                    
                </div>

            </div>

            <div class="row we-Footer-section we-Footer-section--sub">
                <div class="we-Footer-section-item">
                    <span class="text-uppercase text-muted">© 2018 All rights reserved</span>
                </div>
                <div class="we-Footer-section-item">
                    <a href="#" class="text-uppercase text-muted">Terms of use & privacy policy</a>
                </div>
            </div>

            <div class="row">
                <div class="col-md-12">
                    <div class="text-center">
                        <a href="#top" class="btn btn-action btn-action-up btn-primary">Ride to the top</a>
                    </div>
                </div>
            </div>

        </div>
    </footer>

</div>

</div></div>

</div>

<script type="text/javascript" src="/etc.clientlibs/clientlibs/granite/jquery-ui.js"></script>
<script type="text/javascript" src="/etc.clientlibs/weretail/clientlibs/clientlib-base.js"></script>
     
    </body>
</html>

```

### JSON {#json}

```
{  
   "designPath":"/libs/settings/wcm/designs/default",
   "title":"Equipment",
   "lastModifiedDate":1515678594528,
   "templateName":"hero-page",
   "cssClassNames":"page",
   "language":"en",
   ":type":"core/wcm/sandbox/components/page/v2/page",
   ":items":{  
      "root":{  
         "columnCount":12,
         "gridClassNames":"aem-Grid aem-Grid--12 aem-Grid--default--12",
         ":items":{  
            "header":{  
               "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
               ":type":"weretail/components/structure/header",
               "theme":"inverse"
            },
            "hero_image":{  
               "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
               "smartSizes":[  

               ],
               "smartImages":[  

               ],
               "lazyEnabled":true,
               "title":"Forest Trail",
               "alt":"Cyclist riding mountain bike on rocky trail",
               "src":"/content/we-retail/us/en/equipment/jcr%3acontent/root/hero_image.img.jpeg/1473680813224.jpeg",
               ":type":"core/wcm/sandbox/components/image/v2/image"
            },
            "responsivegrid":{  
               "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
               "columnCount":12,
               "gridClassNames":"aem-Grid aem-Grid--12 aem-Grid--default--12",
               ":items":{  
                  "title":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "type":"h2",
                     "text":"Welcome this is our finest equipment",
                     ":type":"weretail/components/content/title"
                  },
                  "category_teaser":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--6 aem-GridColumn--offset--default--0 aem-GridColumn--default--none",
                     "smartSizes":[  
                        128,
                        256,
                        512,
                        1024,
                        1280,
                        1440,
                        1920,
                        2048
                     ],
                     "smartImages":[  
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser.img.128.jpeg/1473680823274.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser.img.256.jpeg/1473680823274.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser.img.512.jpeg/1473680823274.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser.img.1024.jpeg/1473680823274.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser.img.1280.jpeg/1473680823274.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser.img.1440.jpeg/1473680823274.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser.img.1920.jpeg/1473680823274.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser.img.2048.jpeg/1473680823274.jpeg"
                     ],
                     "lazyEnabled":false,
                     "title":"Hiker Anapurna",
                     "alt":"Hiker on the trek in Himalayas, Anapurna valley, Nepal",
                     "src":"/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser.img.jpeg/1473680823274.jpeg",
                     ":type":"core/wcm/sandbox/components/image/v2/image"
                  },
                  "category_teaser_2082536754":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--6 aem-GridColumn--offset--default--0 aem-GridColumn--default--none",
                     "smartSizes":[  
                        128,
                        256,
                        512,
                        1024,
                        1280,
                        1440,
                        1920,
                        2048
                     ],
                     "smartImages":[  
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_2082536754.img.128.jpeg/1473680831529.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_2082536754.img.256.jpeg/1473680831529.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_2082536754.img.512.jpeg/1473680831529.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_2082536754.img.1024.jpeg/1473680831529.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_2082536754.img.1280.jpeg/1473680831529.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_2082536754.img.1440.jpeg/1473680831529.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_2082536754.img.1920.jpeg/1473680831529.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_2082536754.img.2048.jpeg/1473680831529.jpeg"
                     ],
                     "lazyEnabled":false,
                     "title":"Running Trail Man",
                     "alt":"Trail running man exercising outdoors for fitness",
                     "src":"/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_2082536754.img.jpeg/1473680831529.jpeg",
                     ":type":"core/wcm/sandbox/components/image/v2/image"
                  },
                  "category_teaser_647414391":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--4 aem-GridColumn--offset--default--0 aem-GridColumn--default--none",
                     "smartSizes":[  
                        128,
                        256,
                        512,
                        1024,
                        1280,
                        1440,
                        1920,
                        2048
                     ],
                     "smartImages":[  
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_647414391.img.128.jpeg/1473680769375.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_647414391.img.256.jpeg/1473680769375.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_647414391.img.512.jpeg/1473680769375.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_647414391.img.1024.jpeg/1473680769375.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_647414391.img.1280.jpeg/1473680769375.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_647414391.img.1440.jpeg/1473680769375.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_647414391.img.1920.jpeg/1473680769375.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_647414391.img.2048.jpeg/1473680769375.jpeg"
                     ],
                     "lazyEnabled":false,
                     "title":"Enduro Trail Jump",
                     "alt":"Enduro mountain biking in the forest",
                     "src":"/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_647414391.img.jpeg/1473680769375.jpeg",
                     ":type":"core/wcm/sandbox/components/image/v2/image"
                  },
                  "category_teaser_1341949589":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--4 aem-GridColumn--offset--default--0 aem-GridColumn--default--none",
                     "smartSizes":[  
                        128,
                        256,
                        512,
                        1024,
                        1280,
                        1440,
                        1920,
                        2048
                     ],
                     "smartImages":[  
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_1341949589.img.128.jpeg/1473680798215.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_1341949589.img.256.jpeg/1473680798215.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_1341949589.img.512.jpeg/1473680798215.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_1341949589.img.1024.jpeg/1473680798215.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_1341949589.img.1280.jpeg/1473680798215.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_1341949589.img.1440.jpeg/1473680798215.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_1341949589.img.1920.jpeg/1473680798215.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_1341949589.img.2048.jpeg/1473680798215.jpeg"
                     ],
                     "lazyEnabled":false,
                     "title":"Wave Nicaragua",
                     "alt":"Surfing in Nicaragua",
                     "src":"/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_1341949589.img.jpeg/1473680798215.jpeg",
                     ":type":"core/wcm/sandbox/components/image/v2/image"
                  },
                  "category_teaser_1398042708":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--4 aem-GridColumn--offset--default--0 aem-GridColumn--default--none",
                     "smartSizes":[  
                        128,
                        256,
                        512,
                        1024,
                        1280,
                        1440,
                        1920,
                        2048
                     ],
                     "smartImages":[  
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_1398042708.img.128.jpeg/1473680831357.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_1398042708.img.256.jpeg/1473680831357.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_1398042708.img.512.jpeg/1473680831357.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_1398042708.img.1024.jpeg/1473680831357.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_1398042708.img.1280.jpeg/1473680831357.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_1398042708.img.1440.jpeg/1473680831357.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_1398042708.img.1920.jpeg/1473680831357.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_1398042708.img.2048.jpeg/1473680831357.jpeg"
                     ],
                     "lazyEnabled":false,
                     "title":"Freeride Steep",
                     "alt":"Steep skiing above valley",
                     "src":"/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_1398042708.img.jpeg/1473680831357.jpeg",
                     ":type":"core/wcm/sandbox/components/image/v2/image"
                  },
                  "title_2112313717":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "type":"h2",
                     "text":"Featured products",
                     ":type":"weretail/components/content/title"
                  },
                  "product_grid":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "dateFormatString":"yyyy-MM-dd",
                     "items":[  
                        {  
                           "url":"/content/we-retail/us/en/products/equipment/biking/marin-mountain-bike-shoes.html",
                           "path":"/content/we-retail/us/en/products/equipment/biking/marin-mountain-bike-shoes",
                           "description":null,
                           "title":"Marin Mountain Bike Shoes",
                           "lastModified":1467202863308
                        },
                        {  
                           "url":"/content/we-retail/us/en/products/equipment/running/fleet-cross-training-shoe.html",
                           "path":"/content/we-retail/us/en/products/equipment/running/fleet-cross-training-shoe",
                           "description":null,
                           "title":"Fleet Cross-Training Shoe",
                           "lastModified":1467202856630
                        },
                        {  
                           "url":"/content/we-retail/us/en/products/equipment/biking/sequoia-bike-helmet.html",
                           "path":"/content/we-retail/us/en/products/equipment/biking/sequoia-bike-helmet",
                           "description":null,
                           "title":"Sequoia Bike Helmet",
                           "lastModified":1467202862562
                        },
                        {  
                           "url":"/content/we-retail/us/en/products/equipment/hiking/rios-t-shirt.html",
                           "path":"/content/we-retail/us/en/products/equipment/hiking/rios-t-shirt",
                           "description":null,
                           "title":"Rios T Shirt",
                           "lastModified":1467202860239
                        },
                        {  
                           "url":"/content/we-retail/us/en/products/equipment/surfing/the-stretch-longboard.html",
                           "path":"/content/we-retail/us/en/products/equipment/surfing/the-stretch-longboard",
                           "description":null,
                           "title":"The Stretch Longboard",
                           "lastModified":1467202855060
                        },
                        {  
                           "url":"/content/we-retail/us/en/products/equipment/running/faba-running-pants.html",
                           "path":"/content/we-retail/us/en/products/equipment/running/faba-running-pants",
                           "description":null,
                           "title":"Faba Running Pants",
                           "lastModified":1467202856232
                        }
                     ],
                     "showDescription":false,
                     "showModificationDate":false,
                     "linkItems":false,
                     ":type":"weretail/components/content/productgrid"
                  },
                  "button":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     ":type":"weretail/components/content/button",
                     "linkTo":"/content/we-retail/us/en/products/equipment",
                     "label":"All equipment"
                  },
                  "title_419694046":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "type":"h2",
                     "text":"Winter is coming, get ready",
                     ":type":"weretail/components/content/title"
                  },
                  "category_teaser_643606949":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--6 aem-GridColumn--offset--default--0 aem-GridColumn--default--none",
                     "smartSizes":[  
                        128,
                        256,
                        512,
                        1024,
                        1280,
                        1440,
                        1920,
                        2048
                     ],
                     "smartImages":[  
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_643606949.img.128.jpeg/1473680763953.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_643606949.img.256.jpeg/1473680763953.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_643606949.img.512.jpeg/1473680763953.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_643606949.img.1024.jpeg/1473680763953.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_643606949.img.1280.jpeg/1473680763953.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_643606949.img.1440.jpeg/1473680763953.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_643606949.img.1920.jpeg/1473680763953.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_643606949.img.2048.jpeg/1473680763953.jpeg"
                     ],
                     "lazyEnabled":false,
                     "title":"Freeride Extreme",
                     "alt":"Aggressive powder skiing",
                     "src":"/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_643606949.img.jpeg/1473680763953.jpeg",
                     ":type":"core/wcm/sandbox/components/image/v2/image"
                  },
                  "category_teaser_883210151":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--6 aem-GridColumn--offset--default--0 aem-GridColumn--default--none",
                     "smartSizes":[  
                        128,
                        256,
                        512,
                        1024,
                        1280,
                        1440,
                        1920,
                        2048
                     ],
                     "smartImages":[  
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_883210151.img.128.jpeg/1473680828178.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_883210151.img.256.jpeg/1473680828178.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_883210151.img.512.jpeg/1473680828178.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_883210151.img.1024.jpeg/1473680828178.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_883210151.img.1280.jpeg/1473680828178.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_883210151.img.1440.jpeg/1473680828178.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_883210151.img.1920.jpeg/1473680828178.jpeg",
                        "/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_883210151.img.2048.jpeg/1473680828178.jpeg"
                     ],
                     "lazyEnabled":false,
                     "title":"Freeride Siberia",
                     "alt":"Skiing deep powder in Siberia",
                     "src":"/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_883210151.img.jpeg/1473680828178.jpeg",
                     ":type":"core/wcm/sandbox/components/image/v2/image"
                  }
               },
               ":itemsOrder":[  
                  "title",
                  "category_teaser",
                  "category_teaser_2082536754",
                  "category_teaser_647414391",
                  "category_teaser_1341949589",
                  "category_teaser_1398042708",
                  "title_2112313717",
                  "product_grid",
                  "button",
                  "title_419694046",
                  "category_teaser_643606949",
                  "category_teaser_883210151"
               ],
               ":type":"wcm/foundation/components/responsivegrid"
            },
            "search":{  
               "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
               "resultsSize":10,
               "searchTermMinimumLength":3,
               "results":[  

               ],
               ":type":"core/wcm/sandbox/components/search/v1/search"
            },
            "footer":{  
               "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
               ":type":"weretail/components/structure/footer"
            }
         },
         ":itemsOrder":[  
            "header",
            "hero_image",
            "responsivegrid",
            "search",
            "footer"
         ],
         ":type":"wcm/foundation/components/responsivegrid"
      }
   },
   ":itemsOrder":[  
      "root"
   ]
}
```

## Edit Dialog {#edit-dialog}

Because the component represents the entire page, settings that would normally be in an edit dialog are found in the [Page Properties](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/editing-page-properties.html) window.

## Design Dialog {#design-dialog}

Because the component represents the entire page, the design dialog is accessed via **Page Information -&gt; Page Policy** when editing the page template.

![](assets/screen_shot_2018-04-03at113410.png)

>[!NOTE]
>
>In previous versions of AEM, **Page Policy** was called **Page Design**.

### Properties Tab {#properties-tab}

Using the Page Design window, you can define the client libraries to be loaded as well as the web resources library for the page.

* **Client Libraries**
  This defines the client library categories to load. JavaScript is added at the body end and the CSS is added to the page head.
* **Client Libraries JavaScript Page Head**
  This defines the JavaScript Client library categories to load in the page head.
  * Categories defined here that are also present in the **Client Libraries** field will have JavaScript loaded in the page head instead of at body end.  
  * No CSS will be loaded unless the category is also present in the **Client Libraries** field.

* **Web Resources Client Library**
  The client library category that is used to serve web resources such as favicons.

![](assets/screenshot_2018-10-19at104949.png)

Libraries can be configured for both the **Client Libraries** and **Client Libraries JavaScript Page Head **fields as follows:

* To add a new field click or tap the **Add** button below the fields.
* To remove a field click or tap the trash can icon next to the field to be removed.
* To rearrange the load order, click or tap and drag the handle next to the field to be moved.

For more information about using client-side libraries see [Using Client Side Libraries](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/clientlibs.html).

>[!CAUTION]
>
>The ability to separately define client libraries for the page head was introduced with core components release 2.2.0.

### Styles Tab {#styles-tab}

The Page Component supports the AEM [Style System](authoring.md#component-styling).

## Technical Details {#technical-details}

The latest technical documentation about the Page Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page).

The entire core components project can be downloaded from GitHub.

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md). 
