---
tags:
  - project
related notes:
  - "[[_Intro]]"
---
## fun silly features

These features could be fun to implement and add to the character of the site
	I don't know how difficult some of these are to implement

- [[Combine Abilities#^f8e434|Propaganda]] in chat for anti citizen

- adding a new stock option ([[$APERTURE]])

- Test a voting system for the Advisor Council
	- add an advisor council quick event
	- assign 10 random top 50 players as advisors, change their leaderboard icon and have a secret vote on the next quick event between 3 options
	- the vote is announced to all players and the chosen quick event happens
	- if there is a tie, a random one of the tied events is chosen

- [[Portal Storm]] Timer
	- we can start teasing the portal storm once [[$APERTURE]] fund is in the game
	- after players got used to the fund existing and it has received some investment, drop a storm warning on the site
	- we can test the [[Timer#^89eefc|Fuzzy Timer]] interaction with the science fund


## complex features

- [[Combat System]]
	- I'll run the numbers and deal with balance so you can focus on implementation
		- I've done one iteration of this but will go over it again after finishing this doc (tomorrow)

- [[Overwatch]]
	- ties into your existing [[Anti Citizen]] system and extends it by also watching the stock market and [[Combine Occupation]] Health amount
	- also extends it by introducing some kind of "API allowance" per user that can be modified by effects like [[Combine Abilities]]

## design / graphics

I can efficiently help with anything that is design related - collecting/organizing images / making UI mock-ups / creating icons etc

- [ ] [[UI]]
	- there need to be a number of UI elements added to the site
	- some of these integrate with existing ones ([[Leaderboards]])
		- others are completely new ([[Voting]] / [[Advisor]] Health)

- [ ] [[Leaderboards]]

- [ ] [[Crate Drops]] might need some new icons etc - I can do that



# minimum viable

Some features, while nice, are not crucial, for example [[Medals]] are something that can be added later on (or never)

The most important features for the idea to work are the [[Combat System]] and [[Advisor Council]]







Split into Gameplay Loop periods

1) [x] economy 2.0
	1) new stock system is great!
	2) [ ] new [[$APERTURE]] fund

2) 
	1) [ ] giant [[Timer]] - that triggers the [[Combine Invasion]] event
	2) [ ] some nice portal storm background images
3) 
	1) [ ] [[Combat System]]
		- [ ] UI for in- and outgoing attacks
	2) [ ] [[Combine]] health bar
	3) [ ] Combat Damage [[Chat]] log
	4) [ ] new [[Crate Drops]]
	5) [ ] some Combine Invasion background images
4) 
	1) [ ] [[Overwatch]] system (ties into existing [[Anti Citizen]] system)
		1) [ ] UI that displays [[Overwatch]] state
	2) [ ] remove [[$GLOBALDEFENSIVE]] stock option, destroy all stocks in that fund
	3) [ ] new [[$REBELLION]] stock option
	4) [ ] new [[Advisor]] role
	5) [ ] new [[Voting]] for the Advisor Council
	6) [ ] new encrypted / decrypted [[Combine Language]] font rendering in [[Chat]]
	7) [ ] new [[Crate Drops]]
	8) [ ] some Combine Occupation / Propaganda background images
5) 
	1) [ ] Global Defensive [[Leaderboards]] ( [[Medals]] )
	2) [ ] Rebellion [[Leaderboards]] ( [[Medals]] )
	3) [ ] Combine [[Leaderboards]] ( Time spent as Advisor )
	4) [x] Default Leaderboard ([[Points]])
	5) [ ] Victory background images
