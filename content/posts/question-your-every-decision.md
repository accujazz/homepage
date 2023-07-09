---
title: "Case study: fixing DAU conversion"
date: 2023-05-30T16:31:52+03:00
---

It's quite rare when an update in user flow can lead to a huge change in one of the key metrics. Even more surprising when the changed screen is a standard one, widely used in the industry.

Almost every html5 game website, the games that you can play online without a download, is structured in the same fashion. There is a homepage with a selection of games divided into genres or some other categories, the user finds a game they like and then is presented a game details page with a description, visuals, maybe some user reviews and other info, that in theory should convince the user to click on the "Play" button and convert into an active player.

Operating such a site, we've noticed something weird: the mobile to desktop device ratio for our users was off: 55/45 for website visitors, but only 20% of users who play the game were doing so from a mobile device. Basically, mobile users played much less, than those who used a desktop PC.

While there maybe a number of explanations for such behaviour: games that are not touch friendly or huge loading times, we decided to investigate the site in the first place, 'cause it's cheaper and quicker, than to tinker with each game individually. Maybe the traffic we direct into the games differs and is predominantly desktop? Nope, quite the contrary, it's mostly mobile. Then what happens when the user lands on the site? Let's see.

Mobile device: click on the "Play" button or hero art launches the game.

![Game screen on a mobile device](/img/posts/html5-games-flow-mobile.jpg)

Desktop device: an iframe is automatically started with the page load.

![Game screen on a desktop device](/img/posts/html5-games-flow-desktop.jpg)

Thinking that something is wrong with the game details page on mobile we decided to mimic the desktop behaviour, bypass it and lead users straight to the game's iframe, opened in fullscreen on their mobile device.

The game is loaded without any action from the user. The user can close the game and go to the game detail page tapping on the menu button.

![Changed behaviour on a mobile device](/img/posts/html5-games-flow-mobile-changed.jpg)

This change resulted in DAU growing 300%. The DAU is counted only after the game is fully loaded, which can take from 5 to 45 seconds depending on the game and connection speed, so the users who dropped during the loading process are not counted. Sure, not all of those players would become really active and complete the game tutorial, but nonetheless, at least the game will have a chance to interest players.

Quite a surprise, that we had, what looked like a not that bad standard screen, massively hurt our performance. Again and again, I continue to learn to challenge every decision, even the ones that are accepted as common knowledge and are made on autopilot mode. Hope this post was helpful to you!