# Steam Rocket League adoption
how to get rocket league on steam

## EVEN MORE IMPORTANT THAN BELOW
I recently found a pretty nice project called [BoilR](https://github.com/PhilipK/BoilR) that is waaaaay better than this. Use that instead unless you really want to. Cheers

## NOTE:
I am currently trying to make this a program you can import via Steam immediately.
Bare with me.

## Requirements
 - Steam account and desktop app
 - Epic Games account (Note: you do not need the Epic Games launcher for this tutorial)
 - Python 3.9 or above as "python" in PATH

## Step 0:
If you do not have any of these things, get them.

## Step 1: Getting Legendary
Legendary is an open-source command line version of the Epic games launcher. In this tutorial, we will use a modified version of it that I made.

Go to <[the github releases](https://github.com/NotLawson/rocketleague-steam/releases/tag/v1)> and follow the instructions to download.
Once downloaded, unzip the folder and open the command prompt.

`python -m pip install .`

This will install the launcher code onto your system.

## Step 2: Legendary set up

To set up legendary, go into a command prompt and type:

`python -m legendary.cli auth`

An Epic Games login window should pop up. Login as normal
Now you are logged in.

### Step 2.1: If you have Epic Games installed
If you already have Rocket League install via Epic Games, you can import it with the following command:

`python -m legendary.cli import "Rocket League"`

To test whether it imported, type this command:

`python -m legendary.cli list`

If it has Rocket League there, it is set up

### Step 2.2: If you don't have Epic Games installed
Next, install the game.

`python -m legendary.cli install "Rocket League"`

To test whether it installed, type this command:

`python -m legendary.cli list`

If it has Rocket League there, it is set up properly

## Step 3: Steam time
Go into Steam and select Add game > Add a non-Steam game
Select any program; We will change the details later.

It should pop up in your Steam Library
Right-click on it and select "Properties"

Set the details to the following:

Name and picture: Anything, this only shows up on Steam
Target: python
Start in: Any valid directory
Launch options:  -m legendary.cli launch "Rocket League" --wait
(Note: include the space at the beginning)

In the controller tab, disable steam input.

Click the X

It should work now.
