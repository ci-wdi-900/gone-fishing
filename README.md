# Gone Fishing 🐟

<img src="https://fishingbooker.com/blog/media/hero-lures.jpg" width="500px" />

In this assignment, you'll create a fishing simulator game that lets the user
decide whether to catch or release randomly generated fish.

The goal is to catch the highest value worth of fish to later sell at the fish market. 
With that said, the fisher is only allowed to catch 10 lbs of fish maximum and can
only fish for six hours.

Each fish that the user catches should have a randomly generated name consisting 
of two desciptors and a type of fish (i.e.: `'Enormous Red Trout'`). Additionally,
each fish should have a randomly generated weight and value.

Finally, lets assume that it takes one hour to catch each fish.

## Requirements 📋

* You make at least three commits in git (after completing parts of the project)
* The user is able to 'catch' fish with randomly generated names, weights, and values
* The time of day is shown to the user
* The user can only fish for six hours
* The user can only catch at maximum 10 lbs of fish
* Each turn, the sum of the user's caught fishes' weight and value is displayed
* At the end of the game, all the fish that the user caught are displayed along
with a sum of their weight and value

As long as you work within these requirements, take as many creative liberties as you like!

## Example 📖

```
You've gone fishing! Try to maximize the value of your caught fish. You can fish
for six hours (till 12:00pm) and can catch at most 10 lbs of fish.

==========================================

The time is 6:00am. So far you've caught:
0 fish, 0 lbs, $0.00

You caught a 'Slimy Scaly Bass' weighing 0.24 lbs
and valued at $3.12

Your action: [c]atch or [r]elease?
> c

You chose to keep the fish.

==========================================

The time is 7:00am. So far you've caught:
1 fish, 0.24 lbs, $3.12

You caught a 'Deepsea Finned Salmon' weighing 4.50 lbs
and valued at $9.24

Your action: [c]atch or [r]elease?
> r

You chose to release the fish.

==========================================
```

_Some time later..._

```
==========================================

The time is 11:00am. So far you've caught:
2 fish, 9.8 lbs, $25.30

You caught a 'Purple Bigmouthed Herring' weighing 1.42 lbs
and valued at $0.05

This fish would put you over 10 lbs, so you release it.

Press [enter] to continue.
>

==========================================

The time is 12:00pm. Times up!

You caught 2 fish:
* Slimy Scaly Bass, 0.24 lbs, $3.12
* Grey Bottom-dwelling Angler, 9.56 lbs, $22.18

Total weight: 9.8 lbs
Total value: $25.30

```

## Hints ❓ 

Once again, check out [HINTS.md](HINTS.md) for hints on how to build this.

## Stretch Goals 🚀

### Tune your randomly generated weights

Tune the minimum and maximum values for your randomly generated fish weights to
make the user's catch/release decisions non-trivial.

### Add color to the terminal

Add color to your game using the `chalk` module.

This is an external dependency that can be installed with `npm install chalk`.

From here, you can use it like so:

```
const chalk = require('chalk');

console.log(chalk.blue('Hello world!'));
```

More information on how to use chalk is available here: https://github.com/chalk/chalk

### Add realism to the passing of time

Make the amount of time required to catch a fish vary each time instead of always
taking exactly one hour! Try randomly generating a new time between 15min and 1.5hrs.

### Give the user a chance to catch a golden doubloon

Give the user a 1/10 (or similar) chance to catch a high-value golden doubloon each turn.

Additionally, give them a 1/10 chance to catch a valueless boot!

### Allow the user to chum the water

Add an additional action that allows the user to chum the water with bait. This
should take some amount of time (30min?) but in turn increase the speed at which
fish are biting.

### Allow the user to release fish caught on previous turns

Add a mechanism that allows the user the ability to release fish caught on a
previous turn. That way the fisher won't have to worry about filling up their
net with low-value fish.
