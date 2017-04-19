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

Using the Entity viewer we can drill down by Entity Type and locate indivual items

![Entity Products](/img/content/solution/entity_products.png)

When viewing an Entity you can view the attributes

![Entity Attributes](/img/content/solution/product_view.png)

and the direct links

![Entity Links](/img/content/solution/product_links.png)