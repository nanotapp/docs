---
description: The important number to know when adding your own malt is the extract number
---

# Adding new malts

This document is based on this [blog post](https://famouslastworts.com/2019/05/24/calculating-potential-extract-from-malt-coas/?fbclid=IwAR06mrOklbeq7c9B_v7orOXN582TbV8XbREWxe7ge_Nzu1Guya77JgZzcMA) by Chris Saunders.

## Calculating Potential Extract for Brewfather from Malt COAs

How much sugar \(extract\) can we get from malt? When we first start learning to brew the numbers seem like magic and try out best to use what our software or lookup tables \(such as those in Palmer’s “How to Brew”\) for granted. It’s possible to generalize a grain into one of the known categories, but with the rise of new malts and craft malsters those assumptions may end up being further off than expected. The end result? Missing gravity targets. However, calculating potential extract is quite straightforward and only requires a little bit of math.

### Understanding a Malt Certificate of Analysis

![Weyermann Certificate of Analysis for Colonge Malt](https://famouslastworts.files.wordpress.com/2019/05/screenshot-2019-05-24-06.52.25.png?w=800)

In the above Weyermann COA we can see they include a lot of information that brewers can use to understand how a certain malt lot may impact brewhouse performance. In order for us to calculate the potential extract we are interested in two items: **moisture content,extract** and **fine grind – coarse grind difference.**

In the above certificate we are lucky because the malster has provided us with the extract brewers are concerned with; **extract dry basis**. The terminology for this field can vary from maltster, it’s also sometimes known as **extract coarse ground, dry basis**. In either case, we want to be working with the dry basis \(db\) extract and can work backwards from there. As you might guess, the dry basis extract isn’t what we can expect from our grain because there’s still some moisture trapped in the malt. This moisture provides no extract whatsoever, so we will need to calculate what the actual extract of the malt will be. With this information we will be calculating **percent extract coarse grind, as is \(%extract cg, ai\)**.

We also need to know what the **fine grind to coarse grind difference** is, which can sometimes be included on the certificate of analysis. The reason for the difference is because malsters perform their lab mashes \(also known as the congress mash\) on very finely crushed grain. This doesn’t represent the real world because mashing with such highly crushed grain would clog up lauter tuns! Some malsters may provide the difference, however it’s not always provided. Usually the difference between a coarse grind and fine grind won’t be more than 2% extract. A rule of thumb one can use 1% as the fine grind to coarse grind difference

```text
%extract gc,ai = %extract cg,db x (1 - %moisture)
```

From the Weyermann Colonge malt we have the following numbers:

* %extract \(fine grind\) dry basis: 81.6%
* %moisture: 4.2%
* fine grind – coarse grind difference: unknown; use 1%

```text
%extract cg,db = %extract fg,db - 1% = 81.6% - 1% = 80.6% 

%extract cg,ai(WEY Cologne) = 
80.6% x (1 - 4.2%) = 80.6 x (1 - 0.042) = 77.21%
```

So what does this mean? We now know that from every unit of Weyermann Colonge malt we will get 0.7721 units of extract \(sugar\) out of it \(77.21%\).

#### [Spreadsheet to help calculate can be found here](https://docs.google.com/spreadsheets/d/1JcAMBRRWAhd9pZi-c7WgXc6l389Dg6dHjsfl9gluFPg).

## Adding a New Malt to Brewfather

For this example, the Weyermann Colonge malt will be added to the [Brewfather](https://brewfather.app/) database. All that needs to be provided is the coarse grind as is extract. In this example 77.21% is set as Yield, then the Potential SG field is filled in automatically.

![Add new malts from the inventory page, click Fermentables, then Add.](https://famouslastworts.files.wordpress.com/2019/05/screenshot-2019-05-24-07.43.17.png?w=800)

The **ppg**s line up with what was calcuated, which is a great way to validate that the new fermentable has been entered correctly.

### \(Optional\) How Potential/“Homebrew Units”/PPG is calculated

In Brewfather you don't need to do this conversion or calculation, since you can enter the Yield % directly, but it can be usefull for other use cases. 

The most common homebrew unit is **ppg** which stands for **p**oints per **p**ound per **g**allon. There’s another unit that metric users can use called the **pkl** which stands for **p**oints per **k**ilogram per **l**itre. It’s possible to actually calculate out how many ppgs or pkls one would get from their malt however there is an easier way to do it. There’s an adjunct that provides 100% extract and is very well documented in homebrewing books; sucrose!

```text
ppgSucrose = 46 pklSucrose = 384
```

With the known maximum for our homebrew unit of choice, we can figure out what our potential extract will be:

```text
ppgWeyColonge = 46 * 0.7721 = 35.5 (1.036) pklWeyColonge = 384 * 0.7721 = 296.5
```

The potential number in Brewfather is PPG in the format of 1.0XX, so the example above would be 1.036.

## Different Malsters. Different COAs

Every malsters COA will look different, however with armed with the knowledge above it should be possible to find the required information to determine how much sugar a new malt will contribute to a brew. Instead of substituting a specialty pilsner malt from your local micro malster as “Canadian Pilsner Malt” with a note, it can be listed in recipes as the proper malster and product.

## References

* How to Brew \(4th Edition\) John Palmer; Brewers Publications
* A Handbook of Basic Brewing Calculations; Stephen Holle; MBAA

