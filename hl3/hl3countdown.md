


GAME DESIGN GOALS

earth (aka the game) is either in a state of 

- peace, trade and gambling
- impending catastrophy
- war against the combine
- rebellion against the combine occupation

1) story telling (unite behind a common enemy)
2) market volatility (shake up the leaderboard)
3) the number 3
4) new user interest ("I will check back on this site in 2 hours to know wtf that portal storm does")
5) cooperation, coordination


DRAMATURGY

- important announcement: a weak portal storm approaches and will hit earth in 3 hours

- earth prepares its defences, a MILITARY DEFENSE FUND stock is added to the market
- players can invest into this stock to weaken the combine attack or completely defend it


- military is expensive, the initial cost of stock is high
	- this shifts the burden away from new players and onto whales
	- whales need to take calculated risk of over or underinvesting in the defense fund
	- some amount of investment from the whales will flow into the defense fund, giving new players the option to make deals with HLX stocks
	- nudges players to keep some amount of available capital open in case of a portal storm emergency, which also makes players more vulnerable to tomatoes
	- not investing or excessively speculating on the defense fund might lower your reputation with other players



### DISASTER STRIKES

- 3 minutes before it hits, the storm is upgraded to a large storm 
	- (the hidden power level of the storm is now 17, our scientists misjudged the order of magnitude by a factor of x but it'll be fine surely, right??)

- players scramble to invest more stock into the MILITARY DEFENSE FUND

- the storm hits earth
- the DURATION HOUR WAR event follows

from here, there are two outcomes:

A: earth is well defended, the combine attack does some damage to the stock market but ultimately fails (the 7 second defense)

B: the combine are too strong and are here to stay on earth (the 7 hour war)

B will happen if the stock price of HLX stock falls below x amount during the attack
- maybe if it reaches $1?

B triggers the RESISTANCE / HOPE event period which lasts until the combine are defeated

"I want the combine off earth"

- the COMBINE suddenly start regenerating hit points

- the MILITARY DEFENSE FUND is wiped out, all stocks are removed from the game

- the REBELLION FUND is added to the game

- RELEASE GORDON FROM STASIS event is added to crates (0.3% chance)

if the REBELLION stock price gets too high, the COMBINE attack the REBELLION FUND from time to time, dealing significant damage to it

the combine attack to the fund is announced shortly before it happens (3-5 minutes)


a higher stock price for the REBELLION FUND increase the frequency and quality of REBEL ATTACK events

REBEL ATTACKS have a low chance of dealing massively significant damage to the combine for a short amount of time, giving players a window to defeat them

alternatively, Gamba enjoyers may buy crates for a 0.3% chance of getting "FREE GORDON FROM STASIS", giving huge buffs to everything for a short time and basically ending the occupation by himself





DURATION HOUR WAR "COMBAT SYSTEM"

the COMBINE ATTACK FORCE is represented as a health bar on the site

the amount of HP is determined by the magnitude of the storm, as well as the current HLX and DEFENSE FUND stock prices

```
storm_category = random()
storm_magnitude = random()


```


the combine attack reduces the price of HLX and DEFENSE stocks with every market update

the magnitude of damage is scaled by

1) HLX STOCK PRICE (higher stock price increases combine attack power)

2) DEFENSE FUND STOCK PRICE (higher stock price decreases combine attack power)

```

combine_damage = (1.3 * HLX_STOCK_PRICE) - (0.75 * DEFENSE_FUND_STOCK)

combine_damage = min(combine_damage, 0)

```

the DEFENSE FUND is represented as a health bar on the site

its health value is the current stock price divided by the 24h highest stock price

```

defense_fund_hp_max = 

```



```

earth_defense_damage = (1.5 * HLX_STOCK_PRICE) - (0.75 * DEFENSE_FUND_STOCK)

earth_defense_damage = min(combine_damage, 0)

```







THE NUMBER 3 (BONUS MULTIPLIER)

DESIGN GOAL:
- it's the number 3
- it's a memeified combat mechanic
- gives players HOPE to defend the combine

EARTH GLOBAL DEFENSE BUFF @ 333.333

if HLX stock is close to the magic numbers (3k, 33k, 333k, 3.33ml etc): 

idle multipliers are tripled
33% discount on stock purchases

the strength of the multiplier inversely scales with the order of magnitude of the stock price
(low stonks -> big hope)

$3 stock     -->  33333333% buff
$33 stock   -->  333333% buff
$333 stock -->  333% buff
etc

--> this will give players HOPE to defend the attack by rallying together around this price point

--> introduce RISK: a large swing can drop HLX stock below THRESHOLD OF OCCUPATION



the amount of HP of the combine is decreased every stock market update by:

- (during war) being attacked by the MILITARY DEFENSE FUND
- (during occupation) being attacked by REBEL ATTACKS

the amount of stocks (hitpoints) of the combine is increased by

- additional portal storms arriving on earth





PORTAL STORM POWER LEVELS

MINOR: 1-2
MEDIUM: 3-6
HEAVY: 7-21
CATASTROPHICALLY WORLD ENDING: 100-200








>[!note] portal storm (combine invasion)
>
> a [POWER LEVEL] portal storm is approaching earth
> 
>TIMER: 1-12 hours
>  
>DRAMATURGY
>
> 1) a new stock is added (MILITARY DEFENSE FUND)
> 2) the estimate scale of the invasion is known to players (a small portal storm approaches in 2 hours 34 minutes)
> 3) the exact scale is not, a medium sized storm could be power level 3-6
> 
> 4) the combine attack power scales by how invested people are in HLX stocks at the time of the attack
>    
> 5) 


