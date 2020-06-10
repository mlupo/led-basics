
> Open this page at [https://mlupo.github.io/led-basics/](https://mlupo.github.io/led-basics/)

Tutorial contents below:

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



## Use as Extension

This repository can be added as an **extension** in MakeCode.

* open [https://makecode.microbit.org/](https://makecode.microbit.org/)
* click on **New Project**
* click on **Extensions** under the gearwheel menu
* search for **https://github.com/mlupo/led-basics** and import

## Edit this project ![Build status badge](https://github.com/mlupo/led-basics/workflows/MakeCode/badge.svg)

To edit this repository in MakeCode.

* open [https://makecode.microbit.org/](https://makecode.microbit.org/)
* click on **Import** then click on **Import URL**
* paste **https://github.com/mlupo/led-basics** and click import

## Blocks preview

This image shows the blocks code from the last commit in master.
This image may take a few minutes to refresh.

![A rendered view of the blocks](https://github.com/mlupo/led-basics/raw/master/.github/makecode/blocks.png)

#### Metadata (used for search, rendering)

* for PXT/microbit
<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>
