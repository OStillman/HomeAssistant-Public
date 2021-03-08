# Zigbee

![Zigbee Logo](/assets/images/zigbee.jpg)

!!! info "A Note"
    A note about Zigbee: I am using the direct ZHA (Zigbee Home Automation) integration alongside a Sonoff Zigbee Hub flashed with Tasmota. It looked like the best way of getting myself setup at the time (and the cheapest!) but there are many other options out there. Including using Zigbee2MQTT or even going for a Z-Wave integration. Take a look and find which you prefer!

## What is Zigbee?
Zigbee is a communication protocal. Think of it like Wifi but less power hungry, and more direct in it's use. Whereas Wifi is used by most devices we own today, Zigbee is saved for IoT devices which may be running via battery power and simply need to report on an event happening, such as a door opening or closing. Directly Powered Zigbee devices also exist (think lightbulbs) which are still low powered but need to be always on and "listening" for commands to turn on

## Why Zigbee? Why not use Wifi?
There's no direct reason, and it's a topic that's hotly debated on many forums around the internet. I'm turning to Zigbee to try and keep devices away from my Wifi network. As more devices get added to it, there can be congestion caused, so it's largely better to keep these small devices away from Wifi. The benefits are namely:

- Less Congestion on Wifi
- Lower Power usage (espcially important for battery powered devices)
- *Generally* standard protocal

But Wifi has it's own benefits:

- Much cheaper devices (Google ESPHome and you'll see what I mean)
- No Hub Required

You just need to work out what's best for you!

!!! tip
    You can of course have a mixture of devices. At the moment I have Wifi devices for those that are useful to be controlled by Google Home, and Zigbee/Other devices that are not needed to be controlled by Google Home. Of course, in the future I aim to control this further, but it's a good way of looking at it initially

## My Setup
Enough about what Zigbee is, how it works, why it's benefical etc. let's talk about my setup

![Sonoff Zigbee Controller](/assets/images/sonoff_zigbee.jpg)

### The Sonoff Zigbee Controller
Small but mighty! I chose this controller as:

- It was easy to get my hands on - It's on Amazon for £20!
- It's simple to Flash
- It's Wireless (Commnications back to the Pi are done via Wifi) so it can be placed ANYWHERE in the house

#### Configuration
This hub needs to be flashed. I used Tasmota, so I could easily integrate into Home Assistant Zigbee (ZHA). The best guide is one availiable on the [blackadder device repo here](https://zigbee.blakadder.com/Sonoff_ZBBridge.html)  

!!! tip
    This process looks comlpex but it really isn't, just be sure to follow the instructions fully and make sure you have adequate time. Rushing = Frustration!

Kit required:

- USB TTL Converter - I Bought [this one](https://www.amazon.co.uk/WINGONEER-CP2104-Serial-Converter-compatible/dp/B01CYBHM26/ref=sr_1_3?crid=L5XNE56PK4JO&dchild=1&keywords=usb+ttl+converter&qid=1615212171&sprefix=usb+ttl+con%2Caps%2C151&sr=8-3) but you basically just need to ensure there's a 3.3v output option
- Some Wire! - Jumper cables work really well from the USB TTL but you will need some (preferably single core) wire to fit into the tiny holes on the PCB.  

Then just follow the tutorial and you'll have it connected to ZHA in no time