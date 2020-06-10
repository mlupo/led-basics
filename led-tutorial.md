# Let's Make LEDs light up!
			
## Step 1: Show some basic LEDs!

The micro:bit has a 5x5 LED screen, filled with red LEDs! It is up to you to show a fun picture on the screen!
Find the show LEDs block, and pop it into the `on start` block, then draw a simple picture!

``` blocks
basic.showLeds(`
    . # . # .
    . # . # .
    . . . . .
    # . . . #
    . # # # .
    `)
```

## Step 2: Let's get animated!!

If you place multiple `show Leds` one after another in the `on start`, what happens? Stack multiple pitures underneath eachother and find out!

```blocks
basic.showLeds(`
    . # . # .
    . # . # .
    . . . . .
    # . . . #
    . # # # .
    `)
basic.showLeds(`
    . . . . .
    # # . # #
    . . . . .
    # . . . #
    . # # # .
    `)
basic.showLeds(`
    . . . . .
    # # . # #
    . . . . .
    # # # # #
    . . . . .
    `)
```

## Step 3: Picking individual points

Individual points on the screen can be toggled as well! The screen is a 5x5 grid, and the top left corner is point (0,0).
Let's see what happens if we `toggle` an led at a specific point. Find the `toggle x 0 y 0` block, and place it into the `forever` block.

```blocks
basic.forever(function () {
    led.toggle(3, 3)
})
```

## Step 4: Make it random
Lastly, we will decompose our screen by making all the leds toggle randomly!
Find the `pick random` block, and put one into each of the `0`s in the `toggle led` block.

```blocks
basic.forever(function () {
    led.toggle(randint(0, 4), randint(0, 4))
})
```
