# Viraaj's Hexapod Robot





| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Viraaj P | Stuart Hall For Boys | Mechanical/robotic engineering | Incoming 7th grader

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE



# Second Milestone


<iframe width="560" height="315" src="https://www.youtube.com/embed/rxW5v5EISyE?si=iVrA0GKTdf82Tdoz" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

For my second milestone, I finished the whole robot. I added the remote, the WLAN module, and the transceiver wireless module. What the wireless module does is that there is 1 on the remote, and 1 on the arduino. The one on the remote sends a frequency wave to the arduino one which makes the motors move with it. When the hexapod turns on, the frequency wave from the remote sends signals to the arduino allowing the movement. The acrylic plate was used to extend the controller to allow for the battery for it to be placed on. Some challenges I faced when doing this was that my remote could connect to everyone elses exept mine. This was because the address for all of our robots were the same. I changed the address by changing the code * see next line*.robot.setRemote(byte byte0, ....,byte byte04) and then set the remote to the same address, remote.Set(byte byte0, ...., byte byte05). There are 5 bytes in each module. Once this was changed, my remote worked for my hexapod. In my final milestone, I will 3d print a battery holder and I will create a head to put it in. This basketball shaped head will have a speaker inside and it will say commands like, cross, between, behind, defense! 

# First Milestone


<iframe width="560" height="315" src="https://www.youtube.com/embed/801dQZTHeT4?si=0_psskIZ3us-BxwH" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


For my first milestone, I finished the chassis of my hexapod and now it works from my computer. I first screwed in the hors to the top chassis, then to the legs, and then to the feet. Next, I put 2 motors together to create the"hips". Following that, I screwed on the hips and had to make sure all of them were at 90 degrees. After that came the legs and then the feet. On my first attempt, the motors were not at 90 degrees. But after that, I carefully screwed them all in and it turned on perfectly. Some major issues that I faced was when I was assembling the hexapod was that I put all the servo horns flipped incorrectly. Due to this, I had to redo all of the screwing. This took 1 day but was a hassle. Next, because we couldnt use lithuim batterys, I could've  desoldered the battery chassis or connect a new battery source to it. I chose to connect a new 7.5 volt battery to it. It was very hard to make small solders for 2 wires but in the end I got it to work. I did this by getting both wires ready, placed the soldering iron on the solder, melted it, and while it was melted I placed both wires in it and it hardened up and worked. After the small screws, all the other screws were much easier to screw in with the nuts. For my calibration, my angles were off by 10 so I had to re calibrate it and now when I turn it on the whole robot goes to 90 degrees.


# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++

//Remote Code
#ifndef ARDUINO_AVR_UNO
#error Wrong board. Please choose "Arduino/Genuino Uno"
#endif

// Include FNHR (Freenove Hexapod Robot) library
#include <FNHR.h>

FNHRRemote remote;

void setup() {
  // Start remote
  remote.Start();
}

void loop() {
  // Update remote
  remote.Update();
}

```
```c++
//Hexapod code
#ifndef ARDUINO_AVR_MEGA2560
#error Wrong board. Please choose "Arduino/Genuino Mega or Mega 2560"
#endif

// Include FNHR (Freenove Hexapod Robot) library
#include <FNHR.h>

FNHR robot;

void setup() {
  // Start Freenove Hexapod Robot with default function
  robot.Start(true);
}

void loop() {
  // Update Freenove Hexapod Robot
  robot.Update();
}

```

# Bill of Materials
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |

# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.
