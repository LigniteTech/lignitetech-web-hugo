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

Relationships exist between `Product` and `Trade`. Any given instance of trade can itself have relationships with multiple `Settlements` and `Confirmations`. There can also be multiple `Intersystem Breaks` or `Trade Exceptions` associated with the `Trade`