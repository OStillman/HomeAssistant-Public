# Zigbee

![Zigbee Logo](/assets/images/zigbee.jpg)

!!! info "A Note"
    A note about Zigbee: I am using the direct ZHA (Zigbee Home Automation) integration alongside a Sonoff Zigbee Hub flashed with Tasmota. It looked like the best way of getting myself setup at the time (and the cheapest!) but there are many other options out there. Including using Zigbee2MQTT. Take a look and find which you prefer!

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

### TBC
This is currently being built. So I'll leave it there for now