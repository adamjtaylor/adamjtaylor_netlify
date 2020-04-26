---
title: '#tidytuesday: Beer production'
author: ~
date: '2020-04-26'
slug: tidytuesday-beer-production
categories: []
tags: []
---

This year, I'd been keen to find time to do [#tidytuesday](https://github.com/rfordatascience/tidytuesday) more often. This was the first week of 2020 that I was really able to get my teeth into.

![](https://pbs.twimg.com/media/EUnHFPVXkAEN_C6?format=png&name=large)

I chose to look at the beer production data, and after staring at it for a while decided to plot some interesting trends around the explosion in production for consumption on the premises. After trying to hack highlighting selected states by hand I found the `gghighlight` package that did the job for me nicely. To rank the states by growth, I calculated multiple linear regressions run through `purrr::map`.

I didn't take an elegant approach to make the charts for total production and on-premises production with a lot of duplicated code. `patchwork` does a fabulous job of stitching things together nicely, and has almost entirely replaced `cowplot` in my day-to-day work.

Of course, as soon as I posted to Twitter I noticed mistakes and decided to make some refinements: Dropping some low/no production years and switching to log scales - essential for not having the trends of the lower-production states swamped by the big boys!

You can find my code for this and other #tidytuesday efforts on [my GitHub](https://github.com/adamjtaylor/tidytuesday).

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Found some time for a <a href="https://twitter.com/hashtag/tidytuesday?src=hash&amp;ref_src=twsrc%5Etfw">#tidytuesday</a> on beer! Finding fast/slow growth states with purrr🐱📦and broom🧹📦 then plotting with gghighlight 📈🖌️📦 and patchwork 🧑
🎨📦. Pleased with this! <a href="https://t.co/79xqhz2pH7">pic.twitter.com/79xqhz2pH7</a></p>&mdash; Adam J Taylor (@adamjtaylor) <a href="https://twitter.com/adamjtaylor/status/1245452050902769669?ref_src=twsrc%5Etfw">April 1, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
