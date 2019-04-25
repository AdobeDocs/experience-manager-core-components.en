---
title: Navigation Component
seo-title: Navigation Component
description: null
seo-description: The Navigation Component allows users to easily navigate a globalized site structure.
uuid: 616c03fb-39b3-402a-b990-f56c87bc6df4
content-type: reference
topic-tags: authoring
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: da8d67d7-b65e-4041-bc0e-e998f24a68f9
disttype: dist5
gnavtheme: light
groupsectionnavitems: no
hidemerchandisingbar: inherit
hidepromocomponent: inherit
modalsize: 426x240
index: y
internal: n
snippet: y
---

# Navigation Component{#navigation-component}

The Navigation Component allows users to easily navigate a globalized site structure.

## Usage {#usage}

The navigation component allows any navigation hierarchy that can be built from the live copies of a blueprint, from the language copies of a language master, or from a simple tree of pages. It allows users of the page to easily navigate a site structure.

The [edit dialog](#edit-dialog) allows the content author to define the navigation root page along with the depth of navigation. The [design dialog](#design-dialog) allows the template author to define default values for the navigation root and depth.

## Version and Compatibility {#version-and-compatibility}

The current version of the Navigation Component is v1, which was introduced with release 2.0.0 of the Core Components in January 2018, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.3|AEM 6.4|AEM 6.5|
|--- |--- |--- |--- |
|v1|Compatible|Compatible|Compatible|


For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

The following is sample taken from [We.Retail](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html).

### HTML {#html}

```
<nav class="cmp-navigation">
    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-0">
        
    <a href="/content/we-retail/language-masters/en.html" title="English" class="cmp-navigation__item-link">English</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-1">
        
    <a href="/content/we-retail/language-masters/en.html" title="English" class="cmp-navigation__item-link">English</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-2">
        
    <a href="/content/we-retail/language-masters/en/experience.html" title="Experience" class="cmp-navigation__item-link">Experience</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-3">
        
    <a href="/content/we-retail/language-masters/en/experience/arctic-surfing-in-lofoten.html" title="Arctic Surfing In Lofoten" class="cmp-navigation__item-link">Arctic Surfing In Lofoten</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-3">
        
    <a href="/content/we-retail/language-masters/en/experience/hours-of-wilderness.html" title="48 hours of Wilderness" class="cmp-navigation__item-link">48 hours of Wilderness</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-3">
        
    <a href="/content/we-retail/language-masters/en/experience/fly-fishing-the-amazon.html" title="Fly-fishing the Amazon" class="cmp-navigation__item-link">Fly-fishing the Amazon</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-3">
        
    <a href="/content/we-retail/language-masters/en/experience/skitouring.html" title="Skitouring" class="cmp-navigation__item-link">Skitouring</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-3">
        
    <a href="/content/we-retail/language-masters/en/experience/steelhead-and-spines-in-alaska.html" title="Steelhead and Spines in Alaska" class="cmp-navigation__item-link">Steelhead and Spines in Alaska</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-3">
        
    <a href="/content/we-retail/language-masters/en/experience/wester-australia-by-camper-van.html" title="Camping in Western Australia" class="cmp-navigation__item-link">Camping in Western Australia</a>

    </li>

    </ul>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-2">
        
    <a href="/content/we-retail/language-masters/en/men.html" title="Men" class="cmp-navigation__item-link">Men</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-2">
        
    <a href="/content/we-retail/language-masters/en/women.html" title="Women" class="cmp-navigation__item-link">Women</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-2">
        
    <a href="/content/we-retail/language-masters/en/equipment.html" title="Equipment" class="cmp-navigation__item-link">Equipment</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-2">
        
    <a href="/content/we-retail/language-masters/en/about-us.html" title="About Us" class="cmp-navigation__item-link">About Us</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-2">
        
    <a href="/content/we-retail/language-masters/en/products.html" title="Products" class="cmp-navigation__item-link">Products</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-3">
        
    <a href="/content/we-retail/language-masters/en/products/women.html" title="Women" class="cmp-navigation__item-link">Women</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-4">
        
    <a href="/content/we-retail/language-masters/en/products/women/coats.html" title="Coats" class="cmp-navigation__item-link">Coats</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/women/coats/sleek-insulated-coat.html" title="Sleek Insulated Coat" class="cmp-navigation__item-link">Sleek Insulated Coat</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/women/coats/sonja-insulated-jacket.html" title="Sonja Insulated Jacket" class="cmp-navigation__item-link">Sonja Insulated Jacket</a>

    </li>

    </ul>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-4">
        
    <a href="/content/we-retail/language-masters/en/products/women/shirts.html" title="Shirts" class="cmp-navigation__item-link">Shirts</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/women/shirts/rios-t-shirt.html" title="Rios T Shirt" class="cmp-navigation__item-link">Rios T Shirt</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/women/shirts/devi-sleeveless-shirt.html" title="Devi Sleeveless Shirt" class="cmp-navigation__item-link">Devi Sleeveless Shirt</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/women/shirts/soleil-tunic.html" title="Soleil Tunic" class="cmp-navigation__item-link">Soleil Tunic</a>

    </li>

    </ul>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-4">
        
    <a href="/content/we-retail/language-masters/en/products/women/pants.html" title="Pants" class="cmp-navigation__item-link">Pants</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/women/pants/hiking-pants.html" title="Hiking Pants" class="cmp-navigation__item-link">Hiking Pants</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/women/pants/faba-running-pants.html" title="Faba Running Pants" class="cmp-navigation__item-link">Faba Running Pants</a>

    </li>

    </ul>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-4">
        
    <a href="/content/we-retail/language-masters/en/products/women/shorts.html" title="Shorts" class="cmp-navigation__item-link">Shorts</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/women/shorts/fleet-fox-running-shorts.html" title="Fleet Fox Running Shorts" class="cmp-navigation__item-link">Fleet Fox Running Shorts</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/women/shorts/candide-trail-short.html" title="Candide Trail Short" class="cmp-navigation__item-link">Candide Trail Short</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/women/shorts/desert-sky-shorts.html" title="Desert Sky Shorts" class="cmp-navigation__item-link">Desert Sky Shorts</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/women/shorts/bahamas-shorts.html" title="Bahamas Shorts" class="cmp-navigation__item-link">Bahamas Shorts</a>

    </li>

    </ul>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-4">
        
    <a href="/content/we-retail/language-masters/en/products/women/gloves.html" title="Gloves" class="cmp-navigation__item-link">Gloves</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/women/gloves/gloves.html" title="Gloves" class="cmp-navigation__item-link">Gloves</a>

    </li>

    </ul>

    </li>

    </ul>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-3">
        
    <a href="/content/we-retail/language-masters/en/products/men.html" title="Men" class="cmp-navigation__item-link">Men</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-4">
        
    <a href="/content/we-retail/language-masters/en/products/men/coats.html" title="Coats" class="cmp-navigation__item-link">Coats</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/men/coats/portland-hooded-jacket.html" title="Portland Hooded Jacket" class="cmp-navigation__item-link">Portland Hooded Jacket</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/men/coats/brooklyn-coat.html" title="Brooklyn Coat" class="cmp-navigation__item-link">Brooklyn Coat</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/men/coats/el-gordo-down-jacket.html" title="El Gordo Down Jacket" class="cmp-navigation__item-link">El Gordo Down Jacket</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/men/coats/double-breasted-raincoat.html" title="Double Breasted Raincoat" class="cmp-navigation__item-link">Double Breasted Raincoat</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/men/coats/slopeside-coat.html" title="Slopeside Coat" class="cmp-navigation__item-link">Slopeside Coat</a>

    </li>

    </ul>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-4">
        
    <a href="/content/we-retail/language-masters/en/products/men/shirts.html" title="Shirts" class="cmp-navigation__item-link">Shirts</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/men/shirts/eton-short-sleeve-shirt.html" title="Eton Short-Sleeve Shirt" class="cmp-navigation__item-link">Eton Short-Sleeve Shirt</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/men/shirts/amsterdam-short-sleeve-travel-shirt.html" title="Amsterdam Short-Sleeve Travel Shirt" class="cmp-navigation__item-link">Amsterdam Short-Sleeve Travel Shirt</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/men/shirts/laguna-short-sleeve-shirt.html" title="Laguna Short-Sleeve Shirt" class="cmp-navigation__item-link">Laguna Short-Sleeve Shirt</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/men/shirts/expedition-tech-long-sleeved-shirt.html" title="Expedition Tech Long-Sleeved Shirt" class="cmp-navigation__item-link">Expedition Tech Long-Sleeved Shirt</a>

    </li>

    </ul>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-4">
        
    <a href="/content/we-retail/language-masters/en/products/men/pants.html" title="Pants" class="cmp-navigation__item-link">Pants</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/men/pants/analog-dark-wash-jean.html" title="Analog Dark Wash Jean" class="cmp-navigation__item-link">Analog Dark Wash Jean</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/men/pants/trail-model-pants.html" title="Trail Model Pants" class="cmp-navigation__item-link">Trail Model Pants</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/men/pants/tribeca-cargo-pants.html" title="Tribeca Cargo Pants" class="cmp-navigation__item-link">Tribeca Cargo Pants</a>

    </li>

    </ul>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-4">
        
    <a href="/content/we-retail/language-masters/en/products/men/shorts.html" title="Shorts" class="cmp-navigation__item-link">Shorts</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/men/shorts/corona-shorts.html" title="Corona Shorts" class="cmp-navigation__item-link">Corona Shorts</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/men/shorts/buffalo-plaid-shorts.html" title="Buffalo Plaid Shorts" class="cmp-navigation__item-link">Buffalo Plaid Shorts</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/men/shorts/stretch-fatigue-shorts.html" title="Stretch Fatigue Shorts" class="cmp-navigation__item-link">Stretch Fatigue Shorts</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/men/shorts/slot-canyon-active-shorts.html" title="Slot Canyon Active Shorts" class="cmp-navigation__item-link">Slot Canyon Active Shorts</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/men/shorts/pipeline-board-shorts.html" title="Pipeline Board Shorts" class="cmp-navigation__item-link">Pipeline Board Shorts</a>

    </li>

    </ul>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-4">
        
    <a href="/content/we-retail/language-masters/en/products/men/scarfs.html" title="Scarfs" class="cmp-navigation__item-link">Scarfs</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/men/scarfs/zurich-wool-scarf.html" title="Zurich Wool Scarf" class="cmp-navigation__item-link">Zurich Wool Scarf</a>

    </li>

    </ul>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-4">
        
    <a href="/content/we-retail/language-masters/en/products/men/gloves.html" title="Gloves" class="cmp-navigation__item-link">Gloves</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/men/gloves/midweight-fleece-gloves.html" title="Midweight Fleece Gloves" class="cmp-navigation__item-link">Midweight Fleece Gloves</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/men/gloves/classic-leather-gloves.html" title="Classic Leather Gloves" class="cmp-navigation__item-link">Classic Leather Gloves</a>

    </li>

    </ul>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-4">
        
    <a href="/content/we-retail/language-masters/en/products/men/footwear.html" title="Footwear" class="cmp-navigation__item-link">Footwear</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/men/footwear/sussex-rain-boots.html" title="Sussex Rain Boots" class="cmp-navigation__item-link">Sussex Rain Boots</a>

    </li>

    </ul>

    </li>

    </ul>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-3">
        
    <a href="/content/we-retail/language-masters/en/products/equipment.html" title="Equipment" class="cmp-navigation__item-link">Equipment</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-4">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/surfing.html" title="Surfing" class="cmp-navigation__item-link">Surfing</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/surfing/bear-8_8_-longboard.html" title="Bear 8'8&quot; Longboard" class="cmp-navigation__item-link">Bear 8'8" Longboard</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/surfing/the-stretch-longboard.html" title="The Stretch Longboard" class="cmp-navigation__item-link">The Stretch Longboard</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/surfing/rusty-parrot-shortboad.html" title="Rusty Parrot Shortboad" class="cmp-navigation__item-link">Rusty Parrot Shortboad</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/surfing/el-greco-8_-shorty.html" title="El Greco 8' Shorty" class="cmp-navigation__item-link">El Greco 8' Shorty</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/surfing/even-keel-paddleboard.html" title="Even Keel Paddleboard" class="cmp-navigation__item-link">Even Keel Paddleboard</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/surfing/chasing-tail-surfboard.html" title="Chasing Tail Surfboard" class="cmp-navigation__item-link">Chasing Tail Surfboard</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/surfing/the-neutrino.html" title="The Neutrino" class="cmp-navigation__item-link">The Neutrino</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/surfing/pipeline-board-shorts.html" title="Pipeline Board Shorts" class="cmp-navigation__item-link">Pipeline Board Shorts</a>

    </li>

    </ul>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-4">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/running.html" title="Running" class="cmp-navigation__item-link">Running</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/running/faba-running-pants.html" title="Faba Running Pants" class="cmp-navigation__item-link">Faba Running Pants</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/running/spixa-runners.html" title="Spixa Runners" class="cmp-navigation__item-link">Spixa Runners</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/running/bpa-free-water-bottle.html" title="BPA-Free Water Bottle" class="cmp-navigation__item-link">BPA-Free Water Bottle</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/running/fleet-cross-training-shoe.html" title="Fleet Cross-Training Shoe" class="cmp-navigation__item-link">Fleet Cross-Training Shoe</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/running/basa-mp3-player.html" title="Basa MP3 Player" class="cmp-navigation__item-link">Basa MP3 Player</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/running/gomobile-fitness-monitorsmart-music-player.html" title="GoMobile Fitness Monitor/Smart Music Player" class="cmp-navigation__item-link">GoMobile Fitness Monitor/Smart Music Player</a>

    </li>

    </ul>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-4">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/water-sports.html" title="Water Sports" class="cmp-navigation__item-link">Water Sports</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/water-sports/bahamas-shorts.html" title="Bahamas Shorts" class="cmp-navigation__item-link">Bahamas Shorts</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/water-sports/soleil-tunic.html" title="Soleil Tunic" class="cmp-navigation__item-link">Soleil Tunic</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/water-sports/pufferfish-snorkeling-fins.html" title="Pufferfish Snorkeling Fins" class="cmp-navigation__item-link">Pufferfish Snorkeling Fins</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/water-sports/aqua-force-gps-fitness-monitor.html" title="Aqua Force GPS Fitness Monitor" class="cmp-navigation__item-link">Aqua Force GPS Fitness Monitor</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/water-sports/cabana-stripe-towel.html" title="Cabana Stripe Towel" class="cmp-navigation__item-link">Cabana Stripe Towel</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/water-sports/pro-series-swim-goggles.html" title="Pro Series Swim Goggles" class="cmp-navigation__item-link">Pro Series Swim Goggles</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/water-sports/seastar-flip-flops.html" title="Seastar Flip Flops" class="cmp-navigation__item-link">Seastar Flip Flops</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/water-sports/manta-ray-snorkel-and-dive-mask.html" title="Manta Ray Snorkel and Dive Mask" class="cmp-navigation__item-link">Manta Ray Snorkel and Dive Mask</a>

    </li>

    </ul>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-4">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/hiking.html" title="Hiking" class="cmp-navigation__item-link">Hiking</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/hiking/hiking-pants.html" title="Hiking Pants" class="cmp-navigation__item-link">Hiking Pants</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/hiking/fleet-fox-running-shorts.html" title="Fleet Fox Running Shorts" class="cmp-navigation__item-link">Fleet Fox Running Shorts</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/hiking/candide-trail-short.html" title="Candide Trail Short" class="cmp-navigation__item-link">Candide Trail Short</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/hiking/desert-sky-shorts.html" title="Desert Sky Shorts" class="cmp-navigation__item-link">Desert Sky Shorts</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/hiking/rios-t-shirt.html" title="Rios T Shirt" class="cmp-navigation__item-link">Rios T Shirt</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/hiking/hiking-poles.html" title="Hiking Poles" class="cmp-navigation__item-link">Hiking Poles</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/hiking/cuzco.html" title="Cuzco" class="cmp-navigation__item-link">Cuzco</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/hiking/trail-model-pants.html" title="Trail Model Pants" class="cmp-navigation__item-link">Trail Model Pants</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/hiking/corona-shorts.html" title="Corona Shorts" class="cmp-navigation__item-link">Corona Shorts</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/hiking/buffalo-plaid-shorts.html" title="Buffalo Plaid Shorts" class="cmp-navigation__item-link">Buffalo Plaid Shorts</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/hiking/stretch-fatigue-shorts.html" title="Stretch Fatigue Shorts" class="cmp-navigation__item-link">Stretch Fatigue Shorts</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/hiking/slot-canyon-active-shorts.html" title="Slot Canyon Active Shorts" class="cmp-navigation__item-link">Slot Canyon Active Shorts</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/hiking/laguna-short-sleeve-shirt.html" title="Laguna Short-Sleeve Shirt" class="cmp-navigation__item-link">Laguna Short-Sleeve Shirt</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/hiking/expedition-tech-long-sleeved-shirt.html" title="Expedition Tech Long-Sleeved Shirt" class="cmp-navigation__item-link">Expedition Tech Long-Sleeved Shirt</a>

    </li>

    </ul>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-4">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/biking.html" title="Biking" class="cmp-navigation__item-link">Biking</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/biking/sequoia-bike-helmet.html" title="Sequoia Bike Helmet" class="cmp-navigation__item-link">Sequoia Bike Helmet</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/biking/comfort-gel-gloves.html" title="Comfort Gel Gloves" class="cmp-navigation__item-link">Comfort Gel Gloves</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/biking/compact-chain-tool.html" title="Compact Chain Tool" class="cmp-navigation__item-link">Compact Chain Tool</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/biking/blast-mini-pump.html" title="Blast Mini Pump" class="cmp-navigation__item-link">Blast Mini Pump</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/biking/marin-mountain-bike-shoes.html" title="Marin Mountain Bike Shoes" class="cmp-navigation__item-link">Marin Mountain Bike Shoes</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/biking/mx121-sport-pedals.html" title="MX121 Sport Pedals" class="cmp-navigation__item-link">MX121 Sport Pedals</a>

    </li>

    </ul>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-4">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/snow-sports.html" title="Snow Sports" class="cmp-navigation__item-link">Snow Sports</a>

    <ul class="cmp-navigation__group">
        
    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/snow-sports/sleek-insulated-coat.html" title="Sleek Insulated Coat" class="cmp-navigation__item-link">Sleek Insulated Coat</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/snow-sports/flying-snowboard.html" title="Flying Snowboard" class="cmp-navigation__item-link">Flying Snowboard</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/snow-sports/el-gordo-down-jacket.html" title="El Gordo Down Jacket" class="cmp-navigation__item-link">El Gordo Down Jacket</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-5">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/snow-sports/midweight-fleece-gloves.html" title="Midweight Fleece Gloves" class="cmp-navigation__item-link">Midweight Fleece Gloves</a>

    </li>

    </ul>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-4">
        
    <a href="/content/we-retail/language-masters/en/products/equipment/pogo-sticks.html" title="Pogo Sticks" class="cmp-navigation__item-link">Pogo Sticks</a>

    </li>

    </ul>

    </li>

    </ul>

    </li>

    </ul>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-1">
        
    <a href="/content/we-retail/language-masters/de.html" title="Deutsch" class="cmp-navigation__item-link">Deutsch</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-1">
        
    <a href="/content/we-retail/language-masters/fr.html" title="Français" class="cmp-navigation__item-link">Français</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-1">
        
    <a href="/content/we-retail/language-masters/es.html" title="Español" class="cmp-navigation__item-link">Español</a>

    </li>

    <li class="cmp-navigation__item cmp-navigation__item--level-1">
        
    <a href="/content/we-retail/language-masters/it.html" title="Italiano" class="cmp-navigation__item-link">Italiano</a>

    </li>

    </ul>

    </li>

    </ul>
</nav>
```

### JSON {#json}

```
"navigation":{  
                     "columnClassNames":"aem-GridColumn aem-GridColumn--default--12",
                     "items":[  
                        {  
                           "children":[  
                              {  
                                 "children":[  
                                    {  
                                       "children":[  
                                          {  
                                             "children":[  

                                             ],
                                             "level":3,
                                             "active":false,
                                             "url":"/content/we-retail/language-masters/en/experience/arctic-surfing-in-lofoten.html",
                                             "path":"/content/we-retail/language-masters/en/experience/arctic-surfing-in-lofoten",
                                             "description":null,
                                             "title":"Arctic Surfing In Lofoten",
                                             "lastModified":1518025580164
                                          },
                                          {  
                                             "children":[  

                                             ],
                                             "level":3,
                                             "active":false,
                                             "url":"/content/we-retail/language-masters/en/experience/hours-of-wilderness.html",
                                             "path":"/content/we-retail/language-masters/en/experience/hours-of-wilderness",
                                             "description":null,
                                             "title":"48 hours of Wilderness",
                                             "lastModified":1518019112764
                                          },
                                          {  
                                             "children":[  

                                             ],
                                             "level":3,
                                             "active":false,
                                             "url":"/content/we-retail/language-masters/en/experience/fly-fishing-the-amazon.html",
                                             "path":"/content/we-retail/language-masters/en/experience/fly-fishing-the-amazon",
                                             "description":null,
                                             "title":"Fly-fishing the Amazon",
                                             "lastModified":1518018766081
                                          },
                                          {  
                                             "children":[  

                                             ],
                                             "level":3,
                                             "active":false,
                                             "url":"/content/we-retail/language-masters/en/experience/skitouring.html",
                                             "path":"/content/we-retail/language-masters/en/experience/skitouring",
                                             "description":null,
                                             "title":"Skitouring",
                                             "lastModified":1518019875897
                                          },
                                          {  
                                             "children":[  

                                             ],
                                             "level":3,
                                             "active":false,
                                             "url":"/content/we-retail/language-masters/en/experience/steelhead-and-spines-in-alaska.html",
                                             "path":"/content/we-retail/language-masters/en/experience/steelhead-and-spines-in-alaska",
                                             "description":null,
                                             "title":"Steelhead and Spines in Alaska",
                                             "lastModified":1518020233687
                                          },
                                          {  
                                             "children":[  

                                             ],
                                             "level":3,
                                             "active":false,
                                             "url":"/content/we-retail/language-masters/en/experience/wester-australia-by-camper-van.html",
                                             "path":"/content/we-retail/language-masters/en/experience/wester-australia-by-camper-van",
                                             "description":null,
                                             "title":"Camping in Western Australia",
                                             "lastModified":1518020637958
                                          }
                                       ],
                                       "level":2,
                                       "active":false,
                                       "url":"/content/we-retail/language-masters/en/experience.html",
                                       "path":"/content/we-retail/language-masters/en/experience",
                                       "description":"",
                                       "title":"Experience",
                                       "lastModified":1518025687881
                                    },
                                    {  
                                       "children":[  

                                       ],
                                       "level":2,
                                       "active":false,
                                       "url":"/content/we-retail/language-masters/en/men.html",
                                       "path":"/content/we-retail/language-masters/en/men",
                                       "description":null,
                                       "title":"Men",
                                       "lastModified":1457988119339
                                    },
                                    {  
                                       "children":[  

                                       ],
                                       "level":2,
                                       "active":false,
                                       "url":"/content/we-retail/language-masters/en/women.html",
                                       "path":"/content/we-retail/language-masters/en/women",
                                       "description":null,
                                       "title":"Women",
                                       "lastModified":1457988163340
                                    },
                                    {  
                                       "children":[  

                                       ],
                                       "level":2,
                                       "active":false,
                                       "url":"/content/we-retail/language-masters/en/equipment.html",
                                       "path":"/content/we-retail/language-masters/en/equipment",
                                       "description":null,
                                       "title":"Equipment",
                                       "lastModified":1457987985265
                                    },
                                    {  
                                       "children":[  

                                       ],
                                       "level":2,
                                       "active":false,
                                       "url":"/content/we-retail/language-masters/en/about-us.html",
                                       "path":"/content/we-retail/language-masters/en/about-us",
                                       "description":null,
                                       "title":"About Us",
                                       "lastModified":1457864437777
                                    },
                                    {  
                                       "children":[  
                                          {  
                                             "children":[  
                                                {  
                                                   "children":[  
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/women/coats/sleek-insulated-coat.html",
                                                         "path":"/content/we-retail/language-masters/en/products/women/coats/sleek-insulated-coat",
                                                         "description":null,
                                                         "title":"Sleek Insulated Coat",
                                                         "lastModified":1467624886811
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/women/coats/sonja-insulated-jacket.html",
                                                         "path":"/content/we-retail/language-masters/en/products/women/coats/sonja-insulated-jacket",
                                                         "description":null,
                                                         "title":"Sonja Insulated Jacket",
                                                         "lastModified":1467624887465
                                                      }
                                                   ],
                                                   "level":4,
                                                   "active":false,
                                                   "url":"/content/we-retail/language-masters/en/products/women/coats.html",
                                                   "path":"/content/we-retail/language-masters/en/products/women/coats",
                                                   "description":null,
                                                   "title":"Coats",
                                                   "lastModified":1467624886480
                                                },
                                                {  
                                                   "children":[  
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/women/shirts/rios-t-shirt.html",
                                                         "path":"/content/we-retail/language-masters/en/products/women/shirts/rios-t-shirt",
                                                         "description":null,
                                                         "title":"Rios T Shirt",
                                                         "lastModified":1467624888221
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/women/shirts/devi-sleeveless-shirt.html",
                                                         "path":"/content/we-retail/language-masters/en/products/women/shirts/devi-sleeveless-shirt",
                                                         "description":null,
                                                         "title":"Devi Sleeveless Shirt",
                                                         "lastModified":1467624888691
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/women/shirts/soleil-tunic.html",
                                                         "path":"/content/we-retail/language-masters/en/products/women/shirts/soleil-tunic",
                                                         "description":null,
                                                         "title":"Soleil Tunic",
                                                         "lastModified":1467624889587
                                                      }
                                                   ],
                                                   "level":4,
                                                   "active":false,
                                                   "url":"/content/we-retail/language-masters/en/products/women/shirts.html",
                                                   "path":"/content/we-retail/language-masters/en/products/women/shirts",
                                                   "description":null,
                                                   "title":"Shirts",
                                                   "lastModified":1467624887862
                                                },
                                                {  
                                                   "children":[  
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/women/pants/hiking-pants.html",
                                                         "path":"/content/we-retail/language-masters/en/products/women/pants/hiking-pants",
                                                         "description":null,
                                                         "title":"Hiking Pants",
                                                         "lastModified":1467624890099
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/women/pants/faba-running-pants.html",
                                                         "path":"/content/we-retail/language-masters/en/products/women/pants/faba-running-pants",
                                                         "description":null,
                                                         "title":"Faba Running Pants",
                                                         "lastModified":1467624890316
                                                      }
                                                   ],
                                                   "level":4,
                                                   "active":false,
                                                   "url":"/content/we-retail/language-masters/en/products/women/pants.html",
                                                   "path":"/content/we-retail/language-masters/en/products/women/pants",
                                                   "description":null,
                                                   "title":"Pants",
                                                   "lastModified":1467624889942
                                                },
                                                {  
                                                   "children":[  
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/women/shorts/fleet-fox-running-shorts.html",
                                                         "path":"/content/we-retail/language-masters/en/products/women/shorts/fleet-fox-running-shorts",
                                                         "description":null,
                                                         "title":"Fleet Fox Running Shorts",
                                                         "lastModified":1467624890816
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/women/shorts/candide-trail-short.html",
                                                         "path":"/content/we-retail/language-masters/en/products/women/shorts/candide-trail-short",
                                                         "description":null,
                                                         "title":"Candide Trail Short",
                                                         "lastModified":1467624891296
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/women/shorts/desert-sky-shorts.html",
                                                         "path":"/content/we-retail/language-masters/en/products/women/shorts/desert-sky-shorts",
                                                         "description":null,
                                                         "title":"Desert Sky Shorts",
                                                         "lastModified":1467624891797
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/women/shorts/bahamas-shorts.html",
                                                         "path":"/content/we-retail/language-masters/en/products/women/shorts/bahamas-shorts",
                                                         "description":null,
                                                         "title":"Bahamas Shorts",
                                                         "lastModified":1467624892154
                                                      }
                                                   ],
                                                   "level":4,
                                                   "active":false,
                                                   "url":"/content/we-retail/language-masters/en/products/women/shorts.html",
                                                   "path":"/content/we-retail/language-masters/en/products/women/shorts",
                                                   "description":null,
                                                   "title":"Shorts",
                                                   "lastModified":1467624890467
                                                },
                                                {  
                                                   "children":[  
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/women/gloves/gloves.html",
                                                         "path":"/content/we-retail/language-masters/en/products/women/gloves/gloves",
                                                         "description":null,
                                                         "title":"Gloves",
                                                         "lastModified":1467624892440
                                                      }
                                                   ],
                                                   "level":4,
                                                   "active":false,
                                                   "url":"/content/we-retail/language-masters/en/products/women/gloves.html",
                                                   "path":"/content/we-retail/language-masters/en/products/women/gloves",
                                                   "description":null,
                                                   "title":"Gloves",
                                                   "lastModified":1467624892330
                                                }
                                             ],
                                             "level":3,
                                             "active":false,
                                             "url":"/content/we-retail/language-masters/en/products/women.html",
                                             "path":"/content/we-retail/language-masters/en/products/women",
                                             "description":null,
                                             "title":"Women",
                                             "lastModified":1467624886350
                                          },
                                          {  
                                             "children":[  
                                                {  
                                                   "children":[  
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/men/coats/portland-hooded-jacket.html",
                                                         "path":"/content/we-retail/language-masters/en/products/men/coats/portland-hooded-jacket",
                                                         "description":null,
                                                         "title":"Portland Hooded Jacket",
                                                         "lastModified":1467624892952
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/men/coats/brooklyn-coat.html",
                                                         "path":"/content/we-retail/language-masters/en/products/men/coats/brooklyn-coat",
                                                         "description":null,
                                                         "title":"Brooklyn Coat",
                                                         "lastModified":1467624893298
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/men/coats/el-gordo-down-jacket.html",
                                                         "path":"/content/we-retail/language-masters/en/products/men/coats/el-gordo-down-jacket",
                                                         "description":null,
                                                         "title":"El Gordo Down Jacket",
                                                         "lastModified":1467624894016
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/men/coats/double-breasted-raincoat.html",
                                                         "path":"/content/we-retail/language-masters/en/products/men/coats/double-breasted-raincoat",
                                                         "description":null,
                                                         "title":"Double Breasted Raincoat",
                                                         "lastModified":1467624894546
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/men/coats/slopeside-coat.html",
                                                         "path":"/content/we-retail/language-masters/en/products/men/coats/slopeside-coat",
                                                         "description":null,
                                                         "title":"Slopeside Coat",
                                                         "lastModified":1467624894896
                                                      }
                                                   ],
                                                   "level":4,
                                                   "active":false,
                                                   "url":"/content/we-retail/language-masters/en/products/men/coats.html",
                                                   "path":"/content/we-retail/language-masters/en/products/men/coats",
                                                   "description":null,
                                                   "title":"Coats",
                                                   "lastModified":1467624892726
                                                },
                                                {  
                                                   "children":[  
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/men/shirts/eton-short-sleeve-shirt.html",
                                                         "path":"/content/we-retail/language-masters/en/products/men/shirts/eton-short-sleeve-shirt",
                                                         "description":null,
                                                         "title":"Eton Short-Sleeve Shirt",
                                                         "lastModified":1467624895392
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/men/shirts/amsterdam-short-sleeve-travel-shirt.html",
                                                         "path":"/content/we-retail/language-masters/en/products/men/shirts/amsterdam-short-sleeve-travel-shirt",
                                                         "description":null,
                                                         "title":"Amsterdam Short-Sleeve Travel Shirt",
                                                         "lastModified":1467624895791
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/men/shirts/laguna-short-sleeve-shirt.html",
                                                         "path":"/content/we-retail/language-masters/en/products/men/shirts/laguna-short-sleeve-shirt",
                                                         "description":null,
                                                         "title":"Laguna Short-Sleeve Shirt",
                                                         "lastModified":1467624896157
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/men/shirts/expedition-tech-long-sleeved-shirt.html",
                                                         "path":"/content/we-retail/language-masters/en/products/men/shirts/expedition-tech-long-sleeved-shirt",
                                                         "description":null,
                                                         "title":"Expedition Tech Long-Sleeved Shirt",
                                                         "lastModified":1467624896498
                                                      }
                                                   ],
                                                   "level":4,
                                                   "active":false,
                                                   "url":"/content/we-retail/language-masters/en/products/men/shirts.html",
                                                   "path":"/content/we-retail/language-masters/en/products/men/shirts",
                                                   "description":null,
                                                   "title":"Shirts",
                                                   "lastModified":1467624895075
                                                },
                                                {  
                                                   "children":[  
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/men/pants/analog-dark-wash-jean.html",
                                                         "path":"/content/we-retail/language-masters/en/products/men/pants/analog-dark-wash-jean",
                                                         "description":null,
                                                         "title":"Analog Dark Wash Jean",
                                                         "lastModified":1467624897077
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/men/pants/trail-model-pants.html",
                                                         "path":"/content/we-retail/language-masters/en/products/men/pants/trail-model-pants",
                                                         "description":null,
                                                         "title":"Trail Model Pants",
                                                         "lastModified":1467624897477
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/men/pants/tribeca-cargo-pants.html",
                                                         "path":"/content/we-retail/language-masters/en/products/men/pants/tribeca-cargo-pants",
                                                         "description":null,
                                                         "title":"Tribeca Cargo Pants",
                                                         "lastModified":1467624897854
                                                      }
                                                   ],
                                                   "level":4,
                                                   "active":false,
                                                   "url":"/content/we-retail/language-masters/en/products/men/pants.html",
                                                   "path":"/content/we-retail/language-masters/en/products/men/pants",
                                                   "description":null,
                                                   "title":"Pants",
                                                   "lastModified":1467624896692
                                                },
                                                {  
                                                   "children":[  
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/men/shorts/corona-shorts.html",
                                                         "path":"/content/we-retail/language-masters/en/products/men/shorts/corona-shorts",
                                                         "description":null,
                                                         "title":"Corona Shorts",
                                                         "lastModified":1467624898298
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/men/shorts/buffalo-plaid-shorts.html",
                                                         "path":"/content/we-retail/language-masters/en/products/men/shorts/buffalo-plaid-shorts",
                                                         "description":null,
                                                         "title":"Buffalo Plaid Shorts",
                                                         "lastModified":1467624898618
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/men/shorts/stretch-fatigue-shorts.html",
                                                         "path":"/content/we-retail/language-masters/en/products/men/shorts/stretch-fatigue-shorts",
                                                         "description":null,
                                                         "title":"Stretch Fatigue Shorts",
                                                         "lastModified":1467624899230
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/men/shorts/slot-canyon-active-shorts.html",
                                                         "path":"/content/we-retail/language-masters/en/products/men/shorts/slot-canyon-active-shorts",
                                                         "description":null,
                                                         "title":"Slot Canyon Active Shorts",
                                                         "lastModified":1467624899682
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/men/shorts/pipeline-board-shorts.html",
                                                         "path":"/content/we-retail/language-masters/en/products/men/shorts/pipeline-board-shorts",
                                                         "description":null,
                                                         "title":"Pipeline Board Shorts",
                                                         "lastModified":1467624900347
                                                      }
                                                   ],
                                                   "level":4,
                                                   "active":false,
                                                   "url":"/content/we-retail/language-masters/en/products/men/shorts.html",
                                                   "path":"/content/we-retail/language-masters/en/products/men/shorts",
                                                   "description":null,
                                                   "title":"Shorts",
                                                   "lastModified":1467624898030
                                                },
                                                {  
                                                   "children":[  
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/men/scarfs/zurich-wool-scarf.html",
                                                         "path":"/content/we-retail/language-masters/en/products/men/scarfs/zurich-wool-scarf",
                                                         "description":null,
                                                         "title":"Zurich Wool Scarf",
                                                         "lastModified":1467624900804
                                                      }
                                                   ],
                                                   "level":4,
                                                   "active":false,
                                                   "url":"/content/we-retail/language-masters/en/products/men/scarfs.html",
                                                   "path":"/content/we-retail/language-masters/en/products/men/scarfs",
                                                   "description":null,
                                                   "title":"Scarfs",
                                                   "lastModified":1467624900635
                                                },
                                                {  
                                                   "children":[  
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/men/gloves/midweight-fleece-gloves.html",
                                                         "path":"/content/we-retail/language-masters/en/products/men/gloves/midweight-fleece-gloves",
                                                         "description":null,
                                                         "title":"Midweight Fleece Gloves",
                                                         "lastModified":1467624901120
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/men/gloves/classic-leather-gloves.html",
                                                         "path":"/content/we-retail/language-masters/en/products/men/gloves/classic-leather-gloves",
                                                         "description":null,
                                                         "title":"Classic Leather Gloves",
                                                         "lastModified":1467624901414
                                                      }
                                                   ],
                                                   "level":4,
                                                   "active":false,
                                                   "url":"/content/we-retail/language-masters/en/products/men/gloves.html",
                                                   "path":"/content/we-retail/language-masters/en/products/men/gloves",
                                                   "description":null,
                                                   "title":"Gloves",
                                                   "lastModified":1467624900973
                                                },
                                                {  
                                                   "children":[  
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/men/footwear/sussex-rain-boots.html",
                                                         "path":"/content/we-retail/language-masters/en/products/men/footwear/sussex-rain-boots",
                                                         "description":null,
                                                         "title":"Sussex Rain Boots",
                                                         "lastModified":1467624901921
                                                      }
                                                   ],
                                                   "level":4,
                                                   "active":false,
                                                   "url":"/content/we-retail/language-masters/en/products/men/footwear.html",
                                                   "path":"/content/we-retail/language-masters/en/products/men/footwear",
                                                   "description":null,
                                                   "title":"Footwear",
                                                   "lastModified":1467624901568
                                                }
                                             ],
                                             "level":3,
                                             "active":false,
                                             "url":"/content/we-retail/language-masters/en/products/men.html",
                                             "path":"/content/we-retail/language-masters/en/products/men",
                                             "description":null,
                                             "title":"Men",
                                             "lastModified":1467624892633
                                          },
                                          {  
                                             "children":[  
                                                {  
                                                   "children":[  
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/surfing/bear-8_8_-longboard.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/surfing/bear-8_8_-longboard",
                                                         "description":null,
                                                         "title":"Bear 8'8\" Longboard",
                                                         "lastModified":1467624902588
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/surfing/the-stretch-longboard.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/surfing/the-stretch-longboard",
                                                         "description":null,
                                                         "title":"The Stretch Longboard",
                                                         "lastModified":1467624902873
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/surfing/rusty-parrot-shortboad.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/surfing/rusty-parrot-shortboad",
                                                         "description":null,
                                                         "title":"Rusty Parrot Shortboad",
                                                         "lastModified":1467624903161
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/surfing/el-greco-8_-shorty.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/surfing/el-greco-8_-shorty",
                                                         "description":null,
                                                         "title":"El Greco 8' Shorty",
                                                         "lastModified":1467624903449
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/surfing/even-keel-paddleboard.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/surfing/even-keel-paddleboard",
                                                         "description":null,
                                                         "title":"Even Keel Paddleboard",
                                                         "lastModified":1467624903688
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/surfing/chasing-tail-surfboard.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/surfing/chasing-tail-surfboard",
                                                         "description":null,
                                                         "title":"Chasing Tail Surfboard",
                                                         "lastModified":1467624903937
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/surfing/the-neutrino.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/surfing/the-neutrino",
                                                         "description":null,
                                                         "title":"The Neutrino",
                                                         "lastModified":1467624904175
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/surfing/pipeline-board-shorts.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/surfing/pipeline-board-shorts",
                                                         "description":null,
                                                         "title":"Pipeline Board Shorts",
                                                         "lastModified":1467624905781
                                                      }
                                                   ],
                                                   "level":4,
                                                   "active":false,
                                                   "url":"/content/we-retail/language-masters/en/products/equipment/surfing.html",
                                                   "path":"/content/we-retail/language-masters/en/products/equipment/surfing",
                                                   "description":null,
                                                   "title":"Surfing",
                                                   "lastModified":1522319351410
                                                },
                                                {  
                                                   "children":[  
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/running/faba-running-pants.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/running/faba-running-pants",
                                                         "description":null,
                                                         "title":"Faba Running Pants",
                                                         "lastModified":1467624906577
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/running/spixa-runners.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/running/spixa-runners",
                                                         "description":null,
                                                         "title":"Spixa Runners",
                                                         "lastModified":1467624906855
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/running/bpa-free-water-bottle.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/running/bpa-free-water-bottle",
                                                         "description":null,
                                                         "title":"BPA-Free Water Bottle",
                                                         "lastModified":1467624907136
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/running/fleet-cross-training-shoe.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/running/fleet-cross-training-shoe",
                                                         "description":null,
                                                         "title":"Fleet Cross-Training Shoe",
                                                         "lastModified":1467624907579
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/running/basa-mp3-player.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/running/basa-mp3-player",
                                                         "description":null,
                                                         "title":"Basa MP3 Player",
                                                         "lastModified":1467624907865
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/running/gomobile-fitness-monitorsmart-music-player.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/running/gomobile-fitness-monitorsmart-music-player",
                                                         "description":null,
                                                         "title":"GoMobile Fitness Monitor/Smart Music Player",
                                                         "lastModified":1467624908144
                                                      }
                                                   ],
                                                   "level":4,
                                                   "active":false,
                                                   "url":"/content/we-retail/language-masters/en/products/equipment/running.html",
                                                   "path":"/content/we-retail/language-masters/en/products/equipment/running",
                                                   "description":null,
                                                   "title":"Running",
                                                   "lastModified":1467624906408
                                                },
                                                {  
                                                   "children":[  
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/water-sports/bahamas-shorts.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/water-sports/bahamas-shorts",
                                                         "description":null,
                                                         "title":"Bahamas Shorts",
                                                         "lastModified":1467624908826
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/water-sports/soleil-tunic.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/water-sports/soleil-tunic",
                                                         "description":null,
                                                         "title":"Soleil Tunic",
                                                         "lastModified":1467624909806
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/water-sports/pufferfish-snorkeling-fins.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/water-sports/pufferfish-snorkeling-fins",
                                                         "description":null,
                                                         "title":"Pufferfish Snorkeling Fins",
                                                         "lastModified":1467624910737
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/water-sports/aqua-force-gps-fitness-monitor.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/water-sports/aqua-force-gps-fitness-monitor",
                                                         "description":null,
                                                         "title":"Aqua Force GPS Fitness Monitor",
                                                         "lastModified":1467624911204
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/water-sports/cabana-stripe-towel.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/water-sports/cabana-stripe-towel",
                                                         "description":null,
                                                         "title":"Cabana Stripe Towel",
                                                         "lastModified":1467624911501
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/water-sports/pro-series-swim-goggles.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/water-sports/pro-series-swim-goggles",
                                                         "description":null,
                                                         "title":"Pro Series Swim Goggles",
                                                         "lastModified":1467624911863
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/water-sports/seastar-flip-flops.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/water-sports/seastar-flip-flops",
                                                         "description":null,
                                                         "title":"Seastar Flip Flops",
                                                         "lastModified":1467624913063
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/water-sports/manta-ray-snorkel-and-dive-mask.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/water-sports/manta-ray-snorkel-and-dive-mask",
                                                         "description":null,
                                                         "title":"Manta Ray Snorkel and Dive Mask",
                                                         "lastModified":1467624913633
                                                      }
                                                   ],
                                                   "level":4,
                                                   "active":false,
                                                   "url":"/content/we-retail/language-masters/en/products/equipment/water-sports.html",
                                                   "path":"/content/we-retail/language-masters/en/products/equipment/water-sports",
                                                   "description":null,
                                                   "title":"Water Sports",
                                                   "lastModified":1467624908440
                                                },
                                                {  
                                                   "children":[  
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/hiking/hiking-pants.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/hiking/hiking-pants",
                                                         "description":null,
                                                         "title":"Hiking Pants",
                                                         "lastModified":1467624913966
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/hiking/fleet-fox-running-shorts.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/hiking/fleet-fox-running-shorts",
                                                         "description":null,
                                                         "title":"Fleet Fox Running Shorts",
                                                         "lastModified":1467624914484
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/hiking/candide-trail-short.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/hiking/candide-trail-short",
                                                         "description":null,
                                                         "title":"Candide Trail Short",
                                                         "lastModified":1467624915030
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/hiking/desert-sky-shorts.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/hiking/desert-sky-shorts",
                                                         "description":null,
                                                         "title":"Desert Sky Shorts",
                                                         "lastModified":1467624915660
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/hiking/rios-t-shirt.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/hiking/rios-t-shirt",
                                                         "description":null,
                                                         "title":"Rios T Shirt",
                                                         "lastModified":1467624916250
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/hiking/hiking-poles.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/hiking/hiking-poles",
                                                         "description":null,
                                                         "title":"Hiking Poles",
                                                         "lastModified":1467624916644
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/hiking/cuzco.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/hiking/cuzco",
                                                         "description":null,
                                                         "title":"Cuzco",
                                                         "lastModified":1467624916994
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/hiking/trail-model-pants.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/hiking/trail-model-pants",
                                                         "description":null,
                                                         "title":"Trail Model Pants",
                                                         "lastModified":1467624917472
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/hiking/corona-shorts.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/hiking/corona-shorts",
                                                         "description":null,
                                                         "title":"Corona Shorts",
                                                         "lastModified":1467624918060
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/hiking/buffalo-plaid-shorts.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/hiking/buffalo-plaid-shorts",
                                                         "description":null,
                                                         "title":"Buffalo Plaid Shorts",
                                                         "lastModified":1467624918488
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/hiking/stretch-fatigue-shorts.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/hiking/stretch-fatigue-shorts",
                                                         "description":null,
                                                         "title":"Stretch Fatigue Shorts",
                                                         "lastModified":1467624918886
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/hiking/slot-canyon-active-shorts.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/hiking/slot-canyon-active-shorts",
                                                         "description":null,
                                                         "title":"Slot Canyon Active Shorts",
                                                         "lastModified":1467624919388
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/hiking/laguna-short-sleeve-shirt.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/hiking/laguna-short-sleeve-shirt",
                                                         "description":null,
                                                         "title":"Laguna Short-Sleeve Shirt",
                                                         "lastModified":1467624919901
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/hiking/expedition-tech-long-sleeved-shirt.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/hiking/expedition-tech-long-sleeved-shirt",
                                                         "description":null,
                                                         "title":"Expedition Tech Long-Sleeved Shirt",
                                                         "lastModified":1467624920324
                                                      }
                                                   ],
                                                   "level":4,
                                                   "active":false,
                                                   "url":"/content/we-retail/language-masters/en/products/equipment/hiking.html",
                                                   "path":"/content/we-retail/language-masters/en/products/equipment/hiking",
                                                   "description":null,
                                                   "title":"Hiking",
                                                   "lastModified":1467624913848
                                                },
                                                {  
                                                   "children":[  
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/biking/sequoia-bike-helmet.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/biking/sequoia-bike-helmet",
                                                         "description":null,
                                                         "title":"Sequoia Bike Helmet",
                                                         "lastModified":1467624921113
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/biking/comfort-gel-gloves.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/biking/comfort-gel-gloves",
                                                         "description":null,
                                                         "title":"Comfort Gel Gloves",
                                                         "lastModified":1467624921464
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/biking/compact-chain-tool.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/biking/compact-chain-tool",
                                                         "description":null,
                                                         "title":"Compact Chain Tool",
                                                         "lastModified":1467624921711
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/biking/blast-mini-pump.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/biking/blast-mini-pump",
                                                         "description":null,
                                                         "title":"Blast Mini Pump",
                                                         "lastModified":1467624921918
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/biking/marin-mountain-bike-shoes.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/biking/marin-mountain-bike-shoes",
                                                         "description":null,
                                                         "title":"Marin Mountain Bike Shoes",
                                                         "lastModified":1467624922298
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/biking/mx121-sport-pedals.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/biking/mx121-sport-pedals",
                                                         "description":null,
                                                         "title":"MX121 Sport Pedals",
                                                         "lastModified":1467624922605
                                                      }
                                                   ],
                                                   "level":4,
                                                   "active":false,
                                                   "url":"/content/we-retail/language-masters/en/products/equipment/biking.html",
                                                   "path":"/content/we-retail/language-masters/en/products/equipment/biking",
                                                   "description":null,
                                                   "title":"Biking",
                                                   "lastModified":1467624920869
                                                },
                                                {  
                                                   "children":[  
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/snow-sports/sleek-insulated-coat.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/snow-sports/sleek-insulated-coat",
                                                         "description":null,
                                                         "title":"Sleek Insulated Coat",
                                                         "lastModified":1467624923069
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/snow-sports/flying-snowboard.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/snow-sports/flying-snowboard",
                                                         "description":null,
                                                         "title":"Flying Snowboard",
                                                         "lastModified":1467624923363
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/snow-sports/el-gordo-down-jacket.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/snow-sports/el-gordo-down-jacket",
                                                         "description":null,
                                                         "title":"El Gordo Down Jacket",
                                                         "lastModified":1467624924059
                                                      },
                                                      {  
                                                         "children":[  

                                                         ],
                                                         "level":5,
                                                         "active":false,
                                                         "url":"/content/we-retail/language-masters/en/products/equipment/snow-sports/midweight-fleece-gloves.html",
                                                         "path":"/content/we-retail/language-masters/en/products/equipment/snow-sports/midweight-fleece-gloves",
                                                         "description":null,
                                                         "title":"Midweight Fleece Gloves",
                                                         "lastModified":1467624924569
                                                      }
                                                   ],
                                                   "level":4,
                                                   "active":false,
                                                   "url":"/content/we-retail/language-masters/en/products/equipment/snow-sports.html",
                                                   "path":"/content/we-retail/language-masters/en/products/equipment/snow-sports",
                                                   "description":null,
                                                   "title":"Snow Sports",
                                                   "lastModified":1467624922797
                                                },
                                                {  
                                                   "children":[  

                                                   ],
                                                   "level":4,
                                                   "active":false,
                                                   "url":"/content/we-retail/language-masters/en/products/equipment/pogo-sticks.html",
                                                   "path":"/content/we-retail/language-masters/en/products/equipment/pogo-sticks",
                                                   "description":null,
                                                   "title":"Pogo Sticks",
                                                   "lastModified":1522744096978
                                                }
                                             ],
                                             "level":3,
                                             "active":false,
                                             "url":"/content/we-retail/language-masters/en/products/equipment.html",
                                             "path":"/content/we-retail/language-masters/en/products/equipment",
                                             "description":null,
                                             "title":"Equipment",
                                             "lastModified":1467624902297
                                          }
                                       ],
                                       "level":2,
                                       "active":false,
                                       "url":"/content/we-retail/language-masters/en/products.html",
                                       "path":"/content/we-retail/language-masters/en/products",
                                       "description":null,
                                       "title":"Products",
                                       "lastModified":1467624886183
                                    }
                                 ],
                                 "level":1,
                                 "active":false,
                                 "url":"/content/we-retail/language-masters/en.html",
                                 "path":"/content/we-retail/language-masters/en",
                                 "description":null,
                                 "title":"English",
                                 "lastModified":1522750327184
                              },
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "url":"/content/we-retail/language-masters/de.html",
                                 "path":"/content/we-retail/language-masters/de",
                                 "description":null,
                                 "title":"Deutsch",
                                 "lastModified":1522750327185
                              },
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "url":"/content/we-retail/language-masters/fr.html",
                                 "path":"/content/we-retail/language-masters/fr",
                                 "description":null,
                                 "title":"Français",
                                 "lastModified":1522750327185
                              },
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "url":"/content/we-retail/language-masters/es.html",
                                 "path":"/content/we-retail/language-masters/es",
                                 "description":null,
                                 "title":"Español",
                                 "lastModified":1522750327184
                              },
                              {  
                                 "children":[  

                                 ],
                                 "level":1,
                                 "active":false,
                                 "url":"/content/we-retail/language-masters/it.html",
                                 "path":"/content/we-retail/language-masters/it",
                                 "description":null,
                                 "title":"Italiano",
                                 "lastModified":1522750327184
                              }
                           ],
                           "level":0,
                           "active":false,
                           "url":"/content/we-retail/language-masters/en.html",
                           "path":"/content/we-retail/language-masters/en",
                           "description":null,
                           "title":"English",
                           "lastModified":1522750327184
                        }
                     ],
                     ":type":"weretail/components/structure/navigation"
                  },
```

### Technical Details {#technical-details}

The latest technical documentation about the Navigation Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/navigation/v1/navigation).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md. 

>[!NOTE]
>
>As of Core Components release 2.1.0, the Navigation Component supports [schema.org microdata](https://schema.org).

## Edit Dialog {#edit-dialog}

In the edit dialog, the content author can define the root page for navigation and the depth of the navigation structure.

![](assets/screen_shot_2018-04-03at112055.png)

* **Navigation Root**
  The root page, which will be used to generate the navigation tree.
* **Exclude navigation root**
  Exclude the navigation root in the resulting tree, include its descendants only.  
* **Collect all child pages**
  Collect all pages that are descendants of the navigation root.  
* **Navigation Structure Depth**
  Defines how many levels down the navigation tree the component should display relative to the navigation root (only available when **Collect all child pages** is not selected).

## Design Dialog {#design-dialog}

The design dialog allows the template author to set the default values for the navigation root page and navigation depth that are presented to the content authors.

### Properties Tab {#properties-tab}

![](assets/screen_shot_2018-04-03at112357.png)

* **Navigation Root**
  The default value of the root page of the navigation structure, which will be used to generate the navigation tree and defaulted when the content author adds the component to the page.  
* **Exclude navigation root**
  The default value of the option to exclude the navigation root in the resulting tree.  
* **Collect all child pages**
  The default value of the option to collect all pages that are descendants of the navigation root.  
* **Navigation Structure Depth**
  The default value of the navigation structure depth.

### Styles Tab {#styles-tab}

The Navigation Component supports the AEM [Style System](authoring.md#component-styling).