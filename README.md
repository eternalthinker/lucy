# GameDevCore
Game Dev Society UNSW - Core learning repository

## Welcome!
Welcome! Here, you will learn the core basics of Unreal Engine 4 that are relevant to both programmers and designers alike. Let's get started!

### If you need help
The tutorial is designed to give you the basic resources you need to learn on your own, so try to solve any issues you have by yourself first. Google, as well as the Unreal Engine Wiki are both great resources to go to if you're stuck.

That being said, help is at hand. Send a message to Weilon Ying if you're stuck on a particular part of this tutorial. 

## Version Control and Git
You will need to clone (i.e. download) this repository to this computer to progress to the next section.
If you are an experienced programmer, you'll probably already know how to use Git. If this is the case, clone this repository and go to the next section. If not, then read on.

### What is Git?
Git is a version control system. It allows you to back up changes and revert to previous versions of your work with high granularity. More importantly, it allows multiple people to work on the same project together without running the risk of accidentally overwriting files. In simple terms, it is essentially a manual version of Dropbox/Google Drive, with a lot more control. 

### How do I use it?
This repository uses GitHub as the host for this Git repository. GitHub provides a very useful desktop application that makes it easy to get started. Follow these steps to clone this repository:
* Download the desktop application from https://desktop.github.com/
* Install the application and set up a GitHub account if you don't have one yet.
* Navigate to this repository's homepage (https://github.com/WeilonYing/GameDevCore) and click on Open in Desktop (screenshot: https://imgur.com/a/m5nAW)
* Pick a location to clone your repository to. GitHub Desktop should take care of the rest.
* Navigate to the repository in your file browser (http://imgur.com/a/VZFZf). You should be able to find the file GameDevCore.uproject. Open it in Unreal Engine 4 (in Windows, double clicking it should do this).

If Unreal Engine 4 opens it without any issue, then you have successfully cloned this repository. Good job! Let's move onto the next section.

If you're interested in learning Git for the command line, check out this website: https://try.github.io/

## Level Design Basics
When you first open this level, your screen should look something like this: https://imgur.com/a/3w6T1. If you're unfamiliar with the user interface of Unreal Engine 4, please watch this video tutorial here: https://docs.unrealengine.com/latest/INT/Videos/PLZlv_N0_O1gasd4IcOe9Cx9wHoBB7rxFl/w4XlBKeE46E/index.html.

Click on Play and start the game. You will be controlling a humanoid character. Unfortunately, he can't go very far, as the gap to the other side is too wide. Press Escape to exit the game once you're convinced that this is true :P

We need to add a platform to allow the player to get to the other side (https://imgur.com/a/f7mGc). Drag and drop a cube object from the class viewer (https://imgur.com/a/6zwQY), and place it over the gap to allow the player to get across. Use the arrow handles to fine tune its location (make sure you're in translate mode: http://imgur.com/a/rgcgT), and scale it to properly fill in the gap (http://imgur.com/a/Gxly3). Test your game once you're done.

The end result should look like this: http://imgur.com/a/zLGIW

Once you're happy with the result, move on to the next section.

## Adjusting Object Properties
Most of the classes and objects that UE4 provides have properties and attributes that you can change without needing to write a single line of code. Take the SideScrollerCharacter for example (see image: http://imgur.com/a/Fd086).

As seen in the image, the SideScrollerCharacter object is highlighted in the World Outliner. This tells you that this is the current selected object. There is a details pane below the World Outliner, which show all of the properties and attributes you can change for this object.

In the details pane search bar, search "Max Walk Speed". Set the Max Walk Speed property from 600 to 6000 (http://imgur.com/a/N8Uhc). Once you're done, press Play. If done correctly, you'll notice that your character now has a significantly higher maximum speed.

Feel free to tinker around with the other properties. Hint: Your player's acceleration remains the same. How could we make it reach its new maximum speed faster?

Once you're happy with the results, move on to the next section.

## Lighting
Read the Unreal Engine 4 Lighting Tutorials here: https://docs.unrealengine.com/latest/INT/Engine/Rendering/LightingAndShadows/. At the minimum, read Lighting Basics, Light Mobility and Types of Lights.

First off, we're going to disable the sun and the sky in order to experiment with point lights.
* In the World Outliner, CTRL + Click on SkySphereBlueprint, Light Source and AtmosphericFog and set them to be hidden in-game. Click on the eye icon in the World Outliner to also make them invisible in the editor. (http://imgur.com/a/VO1bl)
* In the Modes window, type in "Light" in the search bar. Drag and drop the Point Light from the window into the game. (http://imgur.com/a/B5aRc).
* Repeat until you've lit the area up. Feel free to adjust the radius and attenuation.

While the end result is probably not that impressive, lighting with Point Lights is a common way of simulating small sources of light, such as fire torches, lanterns and light bulbs.

Let's bring back the sky, and create a sunset effect.
* Re-enable Light Source and AtmosphericFog, both in-game and in editor. You should be able to see sunlight and a lit sky (http://imgur.com/a/J2F8b). Delete SkySphereBlueprint from the World Outliner.
* Click on Light Source in the World Outliner, then select the Rotator in the game editor window. You should be able to see the rotator handles (the green, blue red thingy) in the window. (http://imgur.com/a/yMHu1)
* Left click and hold on the green handle, then drag it up or down. If you can't see the sun, keep dragging it and it should appear eventually. (http://imgur.com/a/Q2zcN)
* Adjust the sun so that it's just above the horizon. It should look something like this: http://imgur.com/a/nMOt2
* If the sunlight is too dark, you can adjust the intensity of the light: http://imgur.com/a/rKa2l

## Uploading your changes to Git
If you're an experienced programmer, you probably know how to do this already. If so, make a branch, name it "[your name]-homework", and push it to this repository.

Once you're finished with your work, you'll need to upload your change to GitHub for marking. Because there will most likely be more than one person doing this lesson, you'll need to make a branch, so that you don't affect the master branch. Read this manual chapter for more information on branching https://www.sbf5.com/~cduan/technical/git/git-2.shtml. In fact, read the whole manual if you have time. For more information on branches and/or you wish to do this in the command line, read this tutorial as well: https://www.atlassian.com/git/tutorials/using-branches

Let's make your branch! 
1. Navigate to the GameDevCore repository in GitHub Desktop.
2. Follow the instructions to create a branch here: https://help.github.com/desktop/guides/contributing/creating-a-branch-for-your-work/
3. Name your branch "[your name]-homework"
4. Commit your branch and push it.

If done successfully, you should see your branch appear here: https://github.com/WeilonYing/GameDevCore/branches.

If you don't have permission to create a branch, send me a message (Weilon Ying) and I'll add you to the contributors list. Alternatively, you may choose to make a fork of this project and add it to your own GitHub profile.

That's it! Good job :)


