# Zigbee

![Zigbee Logo](/assets/images/zigbee.jpg)

## What is Zigbee?

Zigbee is a Wireless Communication Protocal that's used in low-power IoT devices to send messages and report states. 

It's just one of the many communication methods used within IoT:

- Zigbee - The one I use, mostly because of great implementations, plethora of devices out there, fairly cheap to implement
- Z-Wave - Alike to Zigbee, but I beleive better distance
- Wi-Fi - I'm always unsure about this. If you HAVE to use Wi-Fi just watch for "phoning home" devices. Plus, not the lowest of power use! Google "Esp Home"!
- 400(ish)mhz - It's likely how your doorbells work. There's a lot of cheap implementations of this that work by maxing out your Pi, so I'd investigate a more efficient method before taking this route

## My Setup
I keep my Zigbee network simple! Sonoff + Zigbee Home Assistant Add-on!

<figure>
  <img src="./assets/images/sonoff_zigbee.jpg" width="400" />
</figure>

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

#### Why not Zigbee2MQTT?

This decision was mostly made due to device availiability. I.e. wait 3 months for a Zigbee Stick made by some random dude, or Amazon a cheaper Zigbee Hub and get it the next day (I thnk we all know what I chose - Both!)

ZHA Has it's own Benefits:

- Built right into ZHA
- UI Based
- Used with Sonoff Zigbee Hub means the Pi and Zigbee hub can be in two different locations!

But ZHA also has drawbacks:

- Less Device Support!
- Reliance on Home Assistant

Zigbee2MQTT Generally:

- Has more devices
- Uses MQTT instead
- But is CMD based

I've got a Zigbee2MQTT Stick as well which I'm reserving incase I get fed up with ZHA. Currently, that's not looking likely!