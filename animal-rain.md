# Animal Rain

## Step 1 @unplugged
This program will make the Chicken Rain program more flexible by using
something called **arguments** to let you rain whatever type of animals
you program in.

## Step 2
First, add a chat command and call it **rain**.
Press the + button on the command to add an argument, and use the drop-down
menu to rename the argument **animal**.

```blocks
player.onChat("rain", function (animal) {
	
})
```

## Step 3
Put a **repeat** loop into the **rain** command and start out with something
small like 10 times. From **Logic** drag in an **if** block, and an **=**
block, and from **Variables** drag in an **animal** bubble block.

Put all these together inside the loop, so that it reads like this:
**if animal = 1 then**

```blocks
player.onChat("rain", function (animal) {
    for (let index = 0; index < 10; index++) {
        if (animal == 1) {
        }
    }
})
```

## Step 4
Now put a **spawn animal at** block into the **if** block, and change
the middle coordinate to 10, so that it spawns 10 blocks above your head.
Leave the other two numbers at 0.

This will spawn 10 chickens above your head if you run the chat command:
**rain 1** (the '1' will be the first type of animal).

```blocks
player.onChat("rain", function (animal) {
    for (let index = 0; index < 10; index++) {
        if (animal == 1) {
            mobs.spawn(CHICKEN, pos(0, 10, 0))
        }
    }
})
```

## Step 5
Now you can add new options for other types of animals.

Press the **+** button at the bottom of the **if** block *twice*.
Then put in an option for **animal** being equal to 2, and spawn a different
type of animal.
*Leave the else part of the block alone for now.*

```blocks
player.onChat("rain", function (animal) {
    for (let index = 0; index < 10; index++) {
        if (animal == 1) {
            mobs.spawn(CHICKEN, pos(0, 10, 0))
        } else if (animal == 2) {
            mobs.spawn(COW, pos(0, 10, 0))
        } else {
        	
        }
    }
})
```

## Step 6
You can add in as many types of animals as you like by using the **+** button
on the **if** block to add new rules.

Before you do that, add in a **spawn** block to the **else** part of the **if**
block. This means if it doesn't have a rule for the number you chat, or you
forget to put a number in, something will still spawn. Make it spawn something silly
like a salmon.

```blocks
player.onChat("rain", function (animal) {
    for (let index = 0; index < 10; index++) {
        if (animal == 1) {
            mobs.spawn(CHICKEN, pos(0, 10, 0))
        } else if (animal == 2) {
            mobs.spawn(COW, pos(0, 10, 0))
        } else {
            mobs.spawn(SALMON, pos(0, 10, 0))
        }
    }
})
```

## Step 7
Lastly, let's add in a way to change how many animals spawn.
Use the **+** button on the end of your chat command again to add in a
new argument, and rename it to **number**.

From **Variables** drag in the new **number** bubble block and replace the
**10** in your **repeat** block.

You can now chat something like **rain 1 100** to rain down 100 chickens!

```blocks
player.onChat("rain", function (animal, number) {
    for (let index = 0; index < number; index++) {
        if (animal == 1) {
            mobs.spawn(CHICKEN, pos(0, 10, 0))
        } else if (animal == 2) {
            mobs.spawn(COW, pos(0, 10, 0))
        } else {
            mobs.spawn(SALMON, pos(0, 10, 0))
        }
    }
})
```

## Step 8
The last thing to do is to download a copy of your program to import into
your own Minecraft world. Press the **Finish** button to get out of the
tutorial, and then press the **gear** button in the top-right and **save**
your project onto your computer.
![Save your project](https://github.com/Mr-Poulter/resources/blob/main/save_project.png?raw=true)
