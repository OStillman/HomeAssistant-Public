# My Hardware

## Main Server

My Entire SmartHome setup is runnning on a single Pi4 with 2GB of memorry. I got the starter kit from [The PiHut](https://thepihut.com/products/raspberry-pi-starter-kit?variant=20336446046270) and haven't even reached 1/3 of the CPU yet. It's really suprising just how capabale such a small and low powered device can be when you aren't trying to run an OS with a UI!

Of course, the Pi isn't running naked, and I've got what I call "a fairly server-like setup" going on:

- Case: Argon One M.2 - That's right, I'm runnning my Pi on an SSD!
- SSD: Simple 120GB SSD (plenty of storage), no SD card in sight!
- OS: Raspberry Pi OS


### Argon One M.2 Case + SSD
I've opted to run my RPi on an SSD, mainly due to Home Assistant with is famous for killing SD Cards pretty fast, and, as the server is built up, I become more and more reliant on it being up and self-managed!

The [Argon One M.2](https://thepihut.com/products/argon-one-m-2-raspberry-pi-4-case) case is a perfect addition to the Pi:

- It Moves all Ports to the back
- It provides it's own On/Off button, with software as well as hardware shutdown
- It provides heat sync and a heat-controllable fan with an easy to download and install script
- It comes with a M.2 SSD bay, connector and USB adapter to make the connection as non-wire-trailing as possible. 

It's not the cheapest option out there, but I can gurantee it's the best option

I'll also mention I'm technically running a Standard Argon One Case with the M.2 Expansion Panel added 😉

## Other Components
Alongside the Main Server, I have a couple of other Controlling components.

### Raspberry Pi Zero W
This is being used in a REALLY simple manner. Simply stuck to the wall and used as a Teams Status Indicator (i.e. Red = In Meeting, Green = Free)

### Sonoff Zigbee Hub
Brand new and still in the "Testing" phase of use. Seems completely stable and reliable so far. Flashed with Tasmota and benefits from being fully wireless so I can place it in a good location, rather than hidden away like the Pi is. Controls all non-Hue devices (and, currently also the Hue Dimmer Switch)

### Phillips Hue Hub
As it says on the tin. Possibly being replaced by Sonoff, but I need to be able to trust the Sonoff first!

### Google Home
These things are dotted ALL AROUND the house and I'm looking at exposing some Home Assistant Entities to these in the near future