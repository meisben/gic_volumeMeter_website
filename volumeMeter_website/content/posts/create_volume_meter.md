+++
title = '🔉 Creating a volume meter'
date = 2024-01-16T08:05:00Z
draft = false
categories = [ "Full day workshop", "Afternoon workshop" ]
summary = "Let's create the full working volume meter"
+++

---

# Introduction

## Aims
In this part of the activity we will write a program that:
* **Senses**
  * Measusre a sound input
* **Plans**
  * Convert the sound level to a desired output
* **Acts**
  * Commands the motor to move to the desired position

## Learning outcomes

| Learning outcome   |                                                                        |
| ------------------ | ---------------------------------------------------------------------- |
| Sense plan and act | Understand how to use Inputs and Output to achieve the desired outcome |

---

# Preperation

## Equipment required

| Equipment item         | Quantity |
| ---------------------- | :------: |
| Assembled volume meter |    1     |
| Laptop/PC              |    1     |

[![Pic](/images/complete.jpg)](/images/complete.jpg)

---

# Activity

## Introduction

To make the volume meter, we want to measure the sound, then tell the motor to move to a position. The louder the sound the more the motor can move. We can achieve this by dividing the maximum degrees the motor can move by the maximum volume level.

For example if the maximum sound level was `10`, then the for each volume level the sound increased the motor should move by `180/10 = 18` degrees.

If the volume level is `5`, then the motor should move by `180/10 * 5 = 90 degrees`

Another way of saying this is the motor should move by `volume_measured / maximum_volume * maximum_rotation`.

For example if the volume level is `5`, then the motor should move by `5/10 * 180 = 90 degrees`

## Make the volume inidicator move with sound
Let’s create a program to make this work!

* Write the program below
* Make sure you understand how it is functioning
* If you have any questions, feel free to ask a mentor!
* You should now see your motor arm moving proportional to the volume of the sound recorded
  * **Cover** the microbit with your hands gently to **shield it from sound**
  * **Shout** close to the microbit to make a **loud sound**

|                                            Blocks                                            |                                            Python                                            |
| :------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------: |
| [![Pic](/images/motor_move_with_sound_blocks.png)](/images/motor_move_with_sound_blocks.png) | [![Pic](/images/motor_move_with_sound_python.png)](/images/motor_move_with_sound_python.png) |


## Make the indicator move in the correct direction

So our motor is now moving with sound volume!

But you may have noticed that the indicator arm is moving in the wrong direction relative to the numbers! So we need to reverse the direction. How do we do that?

>**Challenge!**
>* *Try and reverse the direction yourself without looking at the code below.*

{{< details "**👉🏾 Hint**" >}}
We need to somehow minus the value we want to move from it’s maximum angle (180 degrees)
{{< /details >}}

|                                                       Blocks                                                       |                                                       Python                                                       |
| :----------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------: |
| [![Pic](/images/motor_move_correctDir_with_sound_blocks.png)](/images/motor_move_correctDir_with_sound_blocks.png) | [![Pic](/images/motor_move_correctDir_with_sound_python.png)](/images/motor_move_correctDir_with_sound_python.png) |