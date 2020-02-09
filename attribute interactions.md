food - NA
mass - random starting values
size - Dependant on: random starting value, mass, can be increased with usage of food(growth)
strength - Dependant on: random starting value, size, can be increased with usage of food(growth)
aggressiveness - Dependant on: random starting value, Size, strength
fightingprowess - Dependant on: random starting value, strength
speed - Dependant on: size, mass, strength
scent - random starting value
senses - random starting value
complacency - Size, mass, random chance
foodfind probability - 
clanvalue - if implemented would allow being to help one another


mass - starting value between 0,100
size - random value between 0,2 * (mass/100)
strength - random starting value between 0,1 * (mass/size) * k             
aggressiveness - random starting value between 1,0 * (strength/k) * (size/c) * fightingprowess
fightingprowess - rsvb 0,1 * (strength) , if the fightingprowess value is < 0 always loses, if both have avoids conflict
speed - rsvb 0,1 * (size/mass) * strength * 1/k
scent - rsvb 0,1
senses - rsvb 0,1
complacency - rsvb 0,1 * (mass/size) * daily food consumption
daily food consumption - rsvb 0,1 * mass 


getfood - order decided on speed, predefined probability whether they find food, limited food per day

conflict - if a being has a high enough aggressiveness value, it can use its senses value to determine whether it will encounter another being, if great disparity in aggressiveness autowin - steal food, otherwise initiate combat, use fightingprowess values, higher value wins, takes food and loser suffers a debuff for random amout of days, reduced aggressiveness, winner increases aggressiveness
