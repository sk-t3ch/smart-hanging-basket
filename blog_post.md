# Smart Hanging Basket

Plants are a fresh and wholesome addition to any home, but can quickly become tiresome …watering plants takes a surprisingly large amount of time, energy and (for me at least) is shockingly hit and miss.

With the T3chFlicks smart hanging basket, you can be lazy and still have beautiful blooms! With just the touch of a button on your Arduino Dashboard, you can water your plants from wherever you are. What’s more, the hanging basket is packed with other cool sensors — view things like weather and light intensity on your dashboard so you can check up on your plant’s environment and get local measurements to help you plan your day (or outfit).

![](https://cdn-images-1.medium.com/max/2160/1*172P4COYwNxMoorEVHn2PA.jpeg)

## Supplies

1. Arduino Maker IoT Bundle: [https://www.distrelec.nl/en/mkr-iot-prime-bundle-...](https://www.distrelec.nl/en/mkr-iot-prime-bundle-arduino-akx00018/p/30142238)

1. 3D Printed parts: [https://gitlab.com/t3chflicks/smart-hanging-basket](https://gitlab.com/t3chflicks/smart-hanging-basket)

1. 12V white led strip: [https://www.distrelec.nl/en/led-strip-12-vdc-bart...](https://www.distrelec.nl/en/led-strip-12-vdc-barthelme-51511328/p/30080262)

1. 5V regulator: [https://www.distrelec.nl/en/ldo-voltage-regulator...](https://www.distrelec.nl/en/ldo-voltage-regulator-5v-1a-to-220-on-semiconductor-mc7805ctg/p/30050400)

1. Power supply: [https://www.distrelec.nl/en/plug-in-power-supply-...](https://www.distrelec.nl/en/plug-in-power-supply-12v-25a-rnd-power-rnd-320-00027/p/30098150)

1. [https://www.distrelec.nl/en/single-travel-adapter-...](https://www.distrelec.nl/en/single-travel-adapter-for-the-uk-protective-contact-fr-pl-be-cz-sk-uk-hk-skross-50023/p/11092263)

1. Connecting clips: [https://amzn.to/2l0gs7X](https://amzn.to/2l0gs7X)

1. Solenoid valve: [https://amzn.to/2n767YG](https://amzn.to/2n767YG)

1. Bolts: [https://amzn.to/2l1hErI](https://amzn.to/2l1hErI)

1. UV transparent plastic: [https://rover.ebay.com/rover/1/710-53481-19255-0/...](https://rover.ebay.com/rover/1/710-53481-19255-0/1?icep_id=114&ipn=icep&toolid=20004&campid=5338601033&mpre=https%3A%2F%2Fwww.ebay.co.uk%2Fitm%2F2-0-mm-Ultra-Transparent-Acrylic-Plexiglass-Sheet-Photo-Frame-Replacement-Glass%2F283254674819%3FssPageName%3DSTRK%253AMEBIDX%253AIT%26var%3D583742003389%26_trksid%3Dp2060353.m2749.l2649)

1. Wire — [https://amzn.to/2n5lxMR](https://amzn.to/2n5lxMR)

1. 3D printer — [https://amzn.to/2mHGfCf](https://amzn.to/2mHGfCf)

1. Heat gun — [https://amzn.to/2mAHFP4](https://amzn.to/2mAHFP4)

1. Soldering iron — [https://amzn.to/2mGZQT3](https://amzn.to/2mGZQT3)
> # [🔗 Get The Smart Hanging Basket Files On Github 📔](https://github.com/sk-t3ch/smart-hanging-basket)

## Tutorial

<center><iframe width='560' height='315' src ='https://www.youtube.com/embed/$LnUSYzTdc5s' frameborder='0' allowfullscreen></iframe></center>

## Build 🛠️

Before we get onto the make, we wanted to take you through some of our thinking behind the project.

### Background — Design

When we embarked on this planty project, we knew we wanted to make a smart hanging basket but we weren’t entirely sure where to begin. We had a couple of ‘must-haves’ for our smart hanging basket, namely:

* It has to be able to hold the weight of a damp soil/flower-filled basket

* It must house the electronics for the LEDs, sensors and water valve

* It needs to have wired power because a solar solution can’t provide enough energy during the winter months (thanks, England)

* It must have an easy-to-access connection with a hose pipe.

Despite best intentions, our first attempt at a design was a pretty hideous block, but after going back to the drawing board, we produced a refined version which (we think) looks quite good!

For the electronics, the [Arduino MKR IoT bundle](https://www.distrelec.ch/en/mkr-iot-prime-bundle-arduino-akx00018/p/30142238) saved the day — the kit contains lots of sensors which were ideally suited to our purpose.

![](https://cdn-images-1.medium.com/max/2000/1*VOW4IZliKBJ7sYOZzRj3zg.jpeg)

**The Arduino environment shield**

The environment shield on the Arduino kit has sensors for: luminescence, temperature air pressure, humidity and UV (broken down into UVA, UVB and UV index).

These sensors can act like a mini weather station for our hanging basket, giving the user access to accurate, live, local information about weather conditions.

![](https://cdn-images-1.medium.com/max/2000/1*Ie4tlD3af1WdGmTi-oRQJw.jpeg)

**The Arduino relay board**

The relay board contained within the kit means we can easily control higher power devices. We decided we could use this to control water flow to the hanging basket using a 12V solenoid valve and also decided a powerful light — we made one using some 12V LED strips — would be a helpful addition.

![](https://cdn-images-1.medium.com/max/2000/1*1ZVW1rsl-iihf1N1SJJWxQ.jpeg)

We also decided to try out the Arduino cloud platform for this project. In a previous project, we made an [app for displaying real time data](https://www.instructables.com/id/Smart-Buoy/), but honestly, the cloud platform was a much more straightforward way to control our Arduino project and was super user-friendly.

### 3D Printed Parts

There are seven main parts:

1. Main Bracket

1. Body

1. Top (lid)

1. Bracket for valve

1. Connectors for the hose nozzle

1. Light support

1. Light cover

![](https://cdn-images-1.medium.com/max/3840/1*rr6kJxmmd6YSEIWuZNeC5A.png)

We designed these parts ourselves — you can find the files for them [here](https://github.com/sk-t3ch/smart-hanging-basket). We decided to print in [PETG filament](https://amzn.to/2lDsc0q) for improved strength, durability and longevity.

Sadly, the print wasn’t perfect so we used a heat gun to try and heal some of the layer gaps (does anyone know how we can get it to print nicely rather than attack the finished print with pyrotechnics?). We left a slot in the top for a window so the sensors can still see and added some embossed effects on the side to try and make it look a bit prettier.

![](https://cdn-images-1.medium.com/max/3998/1*CQTDUqUklgEjzebt9yTohQ.jpeg)

![](https://cdn-images-1.medium.com/max/3840/1*HsvmzSRLVDs7POP6xzTk7w.png)

![](https://cdn-images-1.medium.com/max/3840/1*D7O1XqvbZmzYkVM--LG1EQ.png)

### Prepping the Water Valve

Take the solenoid valve and screw the wires into terminal on top — one for positive and one for ground. It doesn’t matter which way round they go.

![](https://cdn-images-1.medium.com/max/3998/1*ZvzykLONaL-jxMLoVaOlJw.jpeg)

Make a hole in the plastic lid which covers the wiring for the solenoid valve. Pass the positive and ground wires through this hole.

![](https://cdn-images-1.medium.com/max/3000/1*5kvwXZy8SxJea1gCvJy1pg.jpeg)

The solenoid valve case has a hole where wires would ordinarily come out. As we’ve made the hole in the lid and put the wires through this, we no longer need this. Fill this hole with hot glue (an elegant solution, right?!) so water can’t get in.

OPTIONAL: spray paint everything black for a smooth-looking finish.

![](https://cdn-images-1.medium.com/max/3998/1*iuXQZ6FPG0pOTV73extRvg.jpeg)

Screw the hook for the hanging basket into place at the end of the bracket.

![](https://cdn-images-1.medium.com/max/3998/1*I9fVhwaAjKFcBRoupogcPw.jpeg)

### Arduino Stack

Put the 5V power regulator in the perfboard section of the bottom board (i.e. the relay board). Either side on the relevant pins, put headers that will turn 12V-> 5V for the Arduino.

![](https://cdn-images-1.medium.com/max/3998/1*TZLt988UPMmLpm7vgYwc7A.jpeg)

Make a stack of Arduinos, putting the sensor board into the mkr1010 (Arduino), and the mkr1010 into the relay board.

![](https://cdn-images-1.medium.com/max/3998/1*-addquZry-yM6to7euPCVQ.jpeg)

Plug the wires from the solenoid wires into the relay board: Red to 12V, Black to Common © on Relay normally closed (NC) relay to GND of 12V.

### Flood LEDs

Cut five strips of six LEDs from a strip. Wire the positives and negatives together as shown and glue them onto the thicker of the 3D printed light covers.

![](https://cdn-images-1.medium.com/max/3000/1*CyzmO06x25CTYi_ns3CtUQ.jpeg)

![](https://cdn-images-1.medium.com/max/3000/1*vJ9H-273bX278SKwOL8MNQ.jpeg)

Next, wire up the light by connecting the positive wire from the LED grid to the 12V power supply multiconnector. Connect the negative wire from the LED grid to NC (normally closed) of the relay board. Finally, connect a ground wire from Common on the relay board to the Ground of the 12V power supply multiconnector.

Cover the light with the thinner rectangular 3D printed part.

![](https://cdn-images-1.medium.com/max/3840/1*__rZFy9UQbBwwVdALYQA5w.png)

![](https://cdn-images-1.medium.com/max/3840/1*D-GTOphOw7hzxrwTL5R4Kg.png)

### Signal LED

Connect a 220 Ohm resistor to the ground pin of the RGB LED and then plug it into the GND pin on the top of the stack.

![](https://cdn-images-1.medium.com/max/3840/1*s2g6PTUycZeGDmQZwqIwmg.png)

Connect the R, G, and B positives to pins 3, 4, 5. Heat shrink and cover and push the LED through its hole in the lid.

![](https://cdn-images-1.medium.com/max/5440/1*Q1zkpvAUdaI6mtVw4NwomA.png)

![](https://cdn-images-1.medium.com/max/3840/1*qO5Ebhd1zAomd9TSCwqrkQ.png)

### Connect Power

Connect the 12V and Ground multiconnectors to a euro barrel plug male head.

![](https://cdn-images-1.medium.com/max/5440/1*Q2Iw2xgQhvnj4C2qL64ntw.png)

Plug in the female euro barrel plug head from the 12V supply.

![](https://cdn-images-1.medium.com/max/3840/1*fwvz6vuYERvlYkCGMnN2Dg.png)

### Arduino Cloud

As we mentioned earlier, creating dashboards for your Arduino-based IoT project is made simple by their cloud platform.

![](https://cdn-images-1.medium.com/max/5440/1*QFmXH9s7Up91PDfum2Rk3Q.png)

Go to the [Arduino Cloud ](https://create.arduino.cc/iot/things)and create an account.

Create a new ‘thing’ (an Arduino Cloud connected device).

![](https://cdn-images-1.medium.com/max/5440/1*LGGtcJAZkjjOfT0uMaZG9g.png)

Add properties — these will be the variables you are measuring or monitoring. We added temperature as an example.

![](https://cdn-images-1.medium.com/max/5440/1*EvdxAcpZ7tSH8SRws3mZuw.png)

Open your online sketch editor. You can see that some default connections for updating the variables has been added. These should work fine, but to use the temperature measurement on the ENV shield, you will need to add a bit of code which can be found in the examples on the left hand side of the editor.

![](https://cdn-images-1.medium.com/max/5440/1*dYol9JqXZzhknca6QJr0-A.png)

Enter your WiFi credentials.

![](https://cdn-images-1.medium.com/max/5440/1*7MyCLG2kmtqiOmszMAfLmw.png)

Upload your code and return to the dashboard where, if you have done everything correctly, you should see a live updating value of the new variable.

![](https://cdn-images-1.medium.com/max/5440/1*cal7oFwBzPZFnUYY4ZtgcA.png)

We then went on to add all the other sensors on the device to the Arduino Cloud: temperature, humidity, illuminance, pressure, UVB, UVA. We also added controls for RGB colour of the LED and floodlight and water control. Check out our code to see how we did it.

![](https://cdn-images-1.medium.com/max/5440/1*HoYgCAmyF2OI4M3flGnVqw.png)

### Put Together

Glue the Arduino in place inside the case and tidy up the wires.

![](https://cdn-images-1.medium.com/max/3840/1*z2oAq41iwTXeDRzhsv-dLA.png)

Put the lid on the case and glue on the 10 X 5 cm UV transparent cover.

![](https://cdn-images-1.medium.com/max/3998/1*xrEvO-GSu8Gm8ZsK5LVo8Q.jpeg)

![](https://cdn-images-1.medium.com/max/3840/1*nUcq1cc_poxah6agprMe4Q.png)

Screw the hose-to-solenoid valve connector onto the solenoid valve at the end nearest the wall. Connect the hose to the valve connector.

![](https://cdn-images-1.medium.com/max/3840/1*r2UEkSszqrd5H1EQ4QOKqQ.png)

Screw the nozzle onto the other side of the solenoid valve (i.e. the side nearest the hanging basket hook).

Screw the whole bracket into a wall or fence of your choice (do ask the owner of the vertical surface before you do this…).

![](https://cdn-images-1.medium.com/max/3000/1*Od5QkYzdtkUrOQZkITj7wA.jpeg)

Connect the hose to the tap and turn it on.

Plug in the power supply and sit back as your smart hanging basket means you have green fingers without getting your hands dirty!

![](https://cdn-images-1.medium.com/max/3840/1*4gw2Xeh6Qt_QnIxYtXz56Q.png)

### Use and Admire and Improve

You can now use Arduino creator dashboard to control your [Smart Hanging Basket](https://youtu.be/LnUSYzTdc5s). The app lets you control the floodlight and watering as well as monitor all the sensor readings.

![](https://cdn-images-1.medium.com/max/3840/1*0UlG4LftCEr_ytjRePzHWg.png)

![](https://cdn-images-1.medium.com/max/3840/1*_fzdlTmDAhhLJAagbLXSsQ.png)

There’s a web hooks tap on Arduino Dashboard page that says
‘Webhooks allow you to send and receive automated messages to other services. For example you could use a webhook to receive a notification when a property of your Thing changes. If you’re new to webhooks, check this sample project.’

They don’t seem to have the functionality for ‘receiving automated messages from other services’ from what we can tell, however this would be awesome because you can link your google calendar to IFTTT and automate your watering! If you’re feeling up to challenge of adding it yourself, it is done [here](https://www.instructables.com/id/Irrigation-Using-Google-Calendar/).

You may have noticed that the lid doesn’t sit flush. We fixed this by using some hot glue to fill in the gap (post video) and it works quite well!
> # [🔗 Get The Smart Hanging Basket Files On Github 📔](https://github.com/sk-t3ch/smart-hanging-basket)

## Thanks for reading

![](https://cdn-images-1.medium.com/max/3060/1*tCB7NxpxUUBWDlsLmAJdBg.png)

I hope you have enjoyed this article. If you like the style, check out [T3chFlicks.org](https://t3chflicks.org/) for more tech focused educational content ([YouTube](https://www.youtube.com/channel/UC0eSD-tdiJMI5GQTkMmZ-6w), [Instagram](https://www.instagram.com/t3chflicks/), [Facebook](https://www.facebook.com/t3chflicks), [Twitter](https://twitter.com/t3chflicks)).