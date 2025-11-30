---
tags:
  - game-mechanic
  - combat-system
  - combine
related notes: "[[Combine]]"
---
[[Combine]]

# General Notes on Combat System

The Combat system is inspired by browser games such as [Tribal Wars](https://en.wikipedia.org/wiki/Tribal_Wars) and [X-Wars](https://en.wikipedia.org/wiki/X-Wars) that I played in the late 2000s.

In these games, players build up a village or planet with idle points, trade, form alliances and go to war with other factions.

Combat is done through dispatching units to a village / planet. Troops then travel there for some duration.

The Defender is notified by a list of incoming attack timers. The strength of the attack remains unknown until it arrives.

In these games, combat is determined by a classic RTS rock paper scissors system -

This is where we deviate, since we won't have rock paper scissors unit compositions but instead base calculations on current stock prices.

Players can not manually dispatch these attacks, instead they get dispatched periodically based on current [[$GLOBALDEFENSIVE]] stock prices or from [[Crate Drops]].

>[!note]
>
>the automatic dispatch is partly out of concern of not killing the site from people all spamming a single button.
>If that's something the site can handle (into the future) then a collectively spammable button could be a fun addition to combat



Hence, based on investment in [[$GLOBALDEFENSIVE]], Earth would dispatch some amount of attacks per minute

The Combine Attack Strength is predetermined by the category of the portal storm as well as Earth's investment and [[Global Hope Buff]] levels at [[Portal Storm#^140871|storm dispatch time]].



# Combat Log / UI


Ideally most combat results are displayed in a separate window to not clog up chat

It might be nice to display rare large critical strikes in chat

