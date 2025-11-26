

combine occupation:

`hire_advisor`

converts a random player from the top 20 into an advisor

a combine advisor loses the ability to spend money on the rebel fund or HLX stocks for the duration of being an advisor

other players can free a player by throwing tomatoes at the advisor
players with a low idle multiplier deal additional damage to advisors




`rebel_attack`

with a displayed delay, deals a random amount of damage to the combine

triggered by:

- periodic timer (reduced by a higher rebel stock price)
- crate drops gamba
- gordon freeman is freed from stasis

triggered during:
- combine occupation














`hlx_stock_price = 500k`
`rbl_stock_price = 89k`
`def_stock_price = 100k`

```

HOPE BUFF

// measure distance to nearest 33.3k, 3.3k like number and use it as a multiplier

oom = Order_Of_Magnitude(hlx_stock) // how many zeroes are we at

closest_target_center = 3.33333 * oom
closest_target_higher = 3.33333 * oom * 10
closest_target_lower = 3.33333 * oom / 10

hlx_stock - closest_target_center = 

44k - 33k = 11k
44k - 3k = 41k
44k - 333k = -289,333 // discard negative numbers

11k < 41k --> 11k is the target number


HOPE_BUFF = (closest_target / hlx_stock_price) * 3
HOPE_BUFF = min(HOPE_BUFF, 0.85)

// example

HOPE_BUFF = (333.3k / 500k) * 3
HOPE_BUFF = 0.66 * 3
HOPE_BUFF = 1.998

HOPE_BUFF = (33.3k / 70k) * 3
HOPE_BUFF = 0.42 * 3
HOPE_BUFF = 1.26

HOPE_BUFF = (33.3k / 120k) * 3
HOPE_BUFF = 0.25 * 3
HOPE_BUFF = 0.75
HOPE_BUFF = 0.85 // capped at 0.85 negative hope

HOPE_BUFF = (333k / 333k) * 3
HOPE_BUFF = 1 * 3
HOPE_BUFF = 3 // capped at 3.0 positive hope

// a visual thing here might be to display the HOPE number with a bias towards  being 3
// anything +-0.05 of 3.0 would be displayed as "3"
// this would just be to visually reward earth for reaching high HOPE levels
// otherwise the value would never show the funny number and instead be some random float all the time

```

```


// the rebel attack deals damage based on how much HOPE players are generating
// rebels can deal critical damage

// in this bad for earth example, the combine have a total of 405,020,000 HP



// CRITICAL DAMAGE CALCULATION
// roll all crits and apply the highest one

crit_low_chance = 17%
crit_low_multiplier = 3

crit_high_chance = 3%
crit_high_multiplier = 33



// REBEL DAMAGE CALCULATION


rebel_base_damage = 1000 + RBL_STOCK_PRICE * HOPE
rebel_base_damage = 1000 + 89,000 * 1.6
rebel_base_damage = 143,400

rebel_attack_damage = rebel_base_damage * CRITICAL

rebel_attack_damage = 143,400 // regular damage

rebel_attack_damage = 143,400 * 3.0
rebel_attack_damage = 430,200 // critical hit low (17% chance)

rebel_attack_damage = 143,400 * 333.0
rebel_attack_damage = 47,752,200 // critical hit high (3% chance)

47,752,200 / 405,020,000 = 11.8% of combine max HP

```



```

// DEFENSE FUND DAMAGE CALCULATION


earth_base_damage = 2000

earth_attack_damage = earth_base_damage + (DEF_STOCK_PRICE * HOPE) / 10
earth_attack_damage = 2000 + (285,000 * 2.91) / 10
earth_attack_damage = 83,235

```


```

// DEFENSE FUND MAX HP

earth_base_hp = 50000

earth_max_hp = earth_base_hp + DEF_STOCK_PRICE * 10 * HOPE

earth_max_hp = 50000 + (285,000 * 10 * 2.91)

earth_max_hp = 50000 + 8,293,500

earth_max_hp = 8,343,500

```


```
// COMBINE vs DEFENSE FUND

// COMBINE DAMAGE CALCULATION

combine_base_damage = 6000

combine_attack_damage = combine_base_damage + ((HLX_STOCK_PRICE * (3-HOPE))/3)

combine_attack_damage = 6000 + (285,000 * (3 - 2.91)) / 3
combine_attack_damage = 6000 + (285,000 * 0.09) / 3
combine_attack_damage = 6000 + 8,550 
combine_attack_damage = 14,550

// combine deals low damage if HOPE is high

combine_attack_damage = 6000 + (285,000 * (3 - 0.85)) / 3
combine_attack_damage = 6000 + (285,000 * 2.15) / 3
combine_attack_damage = 204,250



// combine deals high damage if HOPE is low


```


```

// this would be a bad situation for earth
// hlx stock is high which increases the combine's power
// defense fund value is low relative to hlx stock
// the storm magnitude is high (17)

combine_base_hp = 100000

combine_max_hp = combine_base_hp * (hlx_stock_price_24max * storm_mag/2) - (def_stock_price * HOPE)

combine_max_hp = 100000 * ((500k * 8.5) - (100k * 1.998))
combine_max_hp = 405,020,000


// min hp for attacker (prevent negative numbers if defense stock is ultra stonks)


min = combine_base_hp * 17

min = 1000000 * 17
min = 17,000,000

combine_max_hp = min(combine_max_hp, min)

```


```

combine HP regeneration


combine_base_regen = 1000 + (combine_max_hp * 0.01)

// overwatch alertness state gains additional HP regeneration
overwatch_bonus = none, suspicious, alert, hunt_down_the_freeman

suspicious = +0.5% of combine_current_hp
alert = +1.5% of combine_current_hp
hunt_down_the_freeman = +3.0% of combine_max_hp

// players that were hired as advisors provide additional HP regen based on
// their networth (includes current portfolio gains)

advisor_networth = player_points + min(player_portfolio,0)
advisor_regen = advisor_networth * 0.03
// Combine gain 3% of advisor networth as HP regen

all_advisors_regen = sum of all advisor_regen

combine_regen = combine_base_regen + all_advisors_regen + overwatch_bonus


```