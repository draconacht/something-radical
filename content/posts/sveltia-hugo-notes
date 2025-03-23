---
title: notes on integrating SveltiaCMS in Hugo
categories:
  - hugo
  - golang
date: 2025-03-23T18:30:00.000Z
---

. the integration is effectively zero effort. i didn't want to add extra npm build / run steps for my end users, otherwise #tinacms
  was also a frontend i had considered.

. fully local file editing is HUGE for me, probably the biggest reason i didn't use DecapCMS instead. i don't like adding the netlify OAuth dependency and all that entails, and i just wanted a workflow for my users to edit files locally and pass them into a pull request later. it's a bit weird that it's only supported in Chrome/ium, and i hope the file editing API has support for firefox-based browsers in the future.

. lack of custom components hurts a lot. i wanted the ability to have tweet and PDF.js embeds, but there isn't direct support for custom components yet. I ended up making a workaround by using partials that pick up the data from post attributes and embed them directly at the bottom (which is feasible for my specific requirements but probably generally a bad idea)

. no support for Hugo's page bundles is frustrating. i like to organise my assets alongside my posts, although maybe that's more sensible in a VSCode / obsidian workflow than a CMS workflow. had to reorganise my asset files to make it work, and i worry it won't scale well to ~1000 posts (which i don't need anyway). there is category-level asset organisation, but even that is really insufficient

. field customisation is a 10/10 from me. the configs expose all the options that i would've liked, it looks pretty, and there's even support for adding individual pages. custom slugs are great to have too. i would like to see some enum style arrangement for category fields if possible to avoid typos.

. i'm still unfamiliar with the nuances of Hugo, and the template language is quite intimidating to learn (no prior experience with JS components doesn't help). regardless, it was simple enough to hack together some patches onto the theme

. i might want some sort of folder organisation on my admin page in the future, though i don't know if that's already doable with some configuration 😅. the project is not at that scale yet though.
