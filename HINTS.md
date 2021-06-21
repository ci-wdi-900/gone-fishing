# Hints

**After completing each step below, make a commit in git!** This will help you save your progress every time you get your code in a working state.

## Step 1: Foundation

Let's start by creating the foundation of our program. 

Before diving into the specifics of the fishing game, we know that the structure of the fishing
game will require us to create a loop that displays information to the user, then prompts the user for an action.

Start by creating a `main.js` file, installing and importing `prompt-sync`, then creating an infinite loop. Inside that loop,
display some test content to the user (i.e.: 'hello world'), then prompt them for an action. For now you don't need to do anything
with that action.

## Step 2: Generating random fish

Now that we have the foundation of our program, let's build code that will generate a random fish. A random fish will 
need a randomly generated name that consists of two adjectives and a fish-type (i.e.: 'Blue-finned Surface Perch'). Additionally,
each fish will need a random weight and a random dollar value.

While not necessary, I'd reccomend storing all the code to do this in a function. That way when you need to get a new random fish,
you can simply type `const fish = generateRandomFish();`.

### Step 2A: Generating a random fish name

To generate a random name, start by creating three arrays. The first array should contain fish adjectives. 
The second array should contain different fish adjectives. The third array should contain types of fish. Each array should have at least 10 values in it.

Now to generate a random fish name, we'll take a random adjective from the first array, another random adjective from the second array, and a random fish type
from the third array, then put them altogether.

To get a random value from an array, you can generate a random value in between 0 and the last index in the array (`array.length - 1`). To do this, review your solution
to [this assignment](https://github.com/ci-wdi-900/roll-the-dice).

### Step 2B: Generating a random fish weight and value

Now it's time to generate a random weight and value. For this, you might want to generate a random number between 0.00 and 10.00 with two decimal points.

To do this, you could generate a random integer between 0 and 1,000, then divide it by 100.

### Step 2C: Create the fish

Finally, take randomly generated name, weight, and value and store them on an object that represents the fish. This will be extremely helpful
for your organization going forwards.

```
{
    name: 'Blue-finned Surface Perch',
    weight: 4.33,
    value: 2.51
}
```

### Step 2D: Display the fish to the user

With our random fish generation in place, you'll want to randomly generate a fish each iteration of our loop. 
Add some console.logging that displays the fish to the user in a nice looking way.

```
You caught a 'Blue-finned Surface Perch' weighing 
4.33 lbs with a value of $2.51!
```

## Step 3: Allowing the user to catch or release

Now it's time to allow the user to either catch or release the fish. Let's update our `prompt` statement to ask the
user this question. 

Now, depending on the user's answer we need to either catch or release the fish. 

If they choose to release it, that's easy, we do nothing. 

But if they choose to catch it, we need to store it somehow... Let's create an empty array above our while loop definition that will
store fish that the user has caught. If the user chooses to catch the fish, lets `.push` that fish object onto this array.

## Step 4: Displaying the user's total fish

Now that we're storing the user's catch, let's show them some information on the total weight / value of their caught fish.

At the beginning of our while loop, add code that calculates the sums of the caught fishes' weight and value (one or more functions would
be handy for this). Then display these values to the user.

## Step 5: Adding a catch limit

The game requires that we add a 'catch limit' for the user- they shouldn't be able to catch more than 10 lbs of fish. If a fish would
put them over this threshold, we'll automatically release it.

In our while loop, after generating a random fishbut before prompting the user for what to do, determine whether the new fish would put the user
over weight limit.

Now, wrap the part of our code that prompts the user for what to do in a conditional. If they would be over the weight limit, don't prompt them,
simply release the fish (maybe have them press enter to continue as well). Otherwise, carry on as usual and prompt them then handle their choice.

## Step 6: Keeping track of time

Let's add a time component to the game. The user should only be allowed to fish for six hours. Above our while loop, let's create a variable that
stores the hour (`let hour = 6`).

At the start of our while loop, display this time to the user in a friendly way.
```
The time is 6:00am.
```

At the end of our loop, increment the time by one.

Finally, update the condition of the while loop so that after 6 hours (when the time represents noon) the while loop stops looping.

## Step 7: Displaying the final catch

It's time to show the user the final result of their fishing.

Underneath the while loop, write code that displays each fish in a nice way. 
Under that, show the user how many fish they caught, the total weight of their catch, and the total value of their catch.
