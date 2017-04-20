+++
tags = ["finance","trading"]
categories = ["analysis"]
date = "2017-04-19T13:01:11-08:00"
title = "Trade Analytics"
banner = "img/banners/trade-screen.jpg"
+++

# Trade Analytics

## Trade Model

Using a simplified trading model as an example

![Trade Model](/img/content/solution/trade_model.png)

A relationship exists between `Product` and `Trade`. Typically for products can be traded either in multiples (eg Bond, Equity) or individually for OTC.

Any given instance of trade can itself have relationships with multiple `Settlements` and `Confirmations`. There can also be multiple `Intersystem Breaks` or `Trade Exceptions` associated with the `Trade`.

## Data Import

Data can be imported from a variety of sources which can be static, poll based or streaming. For instance we can import from a flat file.

	type::product,source::trading1,productId::2,productType::BondMMDiscount,description::BondMMDiscount Desc
	type::product,source::trading1,productId::3,productType::GenericOption,description::GenericOption Desc
	type::product,source::trading1,productId::4,productType::FX,description::FX Desc
	type::product,source::trading1,productId::5,productType::PositionCash,description::PositionCash Desc
	type::product,source::trading1,productId::6,productType::CommoditySwap2,description::CommoditySwap2 Desc
	type::product,source::trading1,productId::7,productType::CreditDefaultSwap,description::CreditDefaultSwap Desc
	type::product,source::trading1,productId::8,productType::Bond,description::Bond Desc
	type::product,source::trading1,productId::9,productType::PositionCash,description::PositionCash Desc
	type::product,source::trading1,productId::10,productType::FRA,description::FRA Desc

Owing to the flexible data model we can import a variable number of comma delimited key value pairs which are separated by the double colon `::`. Once imported a product will reflect it's attributes in the system.

## Viewing Data

Using the Entity viewer we can drill down by Entity Type and locate indivual items

![Entity Products](/img/content/solution/entity_products.png)

When viewing an Entity you can view the attributes

![Entity Attributes](/img/content/solution/product_view.png)

and the direct links

![Entity Links](/img/content/solution/product_links.png)

## Investigating Data

When you want to gain more insight into your data your first step should be to create a `Workset`. This will allow you to managage entities in groups.

![Workset Overview](/img/content/solution/workset_main.png)

The initial card will give you a brief overview of 

* The number of entities managed
* The total number of attributes 
* The number of active links

Entering the workset you can get an overview of the individal entity attributes by selecting the entity

![Workset Entity Attributes](/img/content/solution/workset_entity_info.png)

Entering the network view allows for the investigation of the links between the entities. 

![Workset Network Depth 0](/img/content/solution/workset_network_depth_0.png)

If a direct link exists then a line will be displayed and the type of relationship will be shown on the line

![Workset Link Text](/img/content/solution/workset_link_text.png)

If you now wish to see the other links for entities you can begin to increase the depth of the relationships using the `Depth Control` for the network view.

![Workset Depth Control](/img/content/solution/workset_depth_control.png)

So, increasing the depth by one allows us to view the immediate neighbours of each of the entities.

![Workset Network Depth 1](/img/content/solution/workset_network_depth_1.png)

You can see that the `Product` is associated with a number of trades, while the `Trade` from the workset has an associated `Settlement` and `Confirmation`

Increasing the depth further brings in the links from the first order neighbours of the original workset.

![Workset Network Depth 2](/img/content/solution/workset_network_depth_2.png)