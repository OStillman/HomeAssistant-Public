# Hue Dimmer Switch

!!! question "Status: Newly Configured"
    The Hue Dimmer Switch has recently been migrated to ZHA and so is undergoing changes

![Hue Dimmer](/assets/images/hue_dimmer.jpg)

## What is a Hue Dimmer?
The Hue Dimmer Switch is a 4 buttoned device aimed at controlling a singular Hue Device/Room. It includes the following buttons:

- On
- Off
- Brighter
- Darker

## Suggested General Configuration
I was unhappy with how Hue tied down the dimmer switch. Control only a specific set of lights, no other controls. It worked, but not the best. So, the best way is to add it to your custom Zigbee Controller to open up (From ZHA):

- Single, Double, Triple, Quadruple & Continous presses of each button
- Flexibilty to control any device you wish
- MOST IMPORTANTLY: Access to If/Else Automations!

!!! info "A Quick Note"
    I'm aware this can be largely achieved via the standard Hue Integration, but at 5 second polling time, this isn't always the best!

!!! warning "Be Aware!"
    On initial pair of your Hue Device, all that will be shown is the battery percentage. Automation Triggers will give you access to the different button actions availiable in whichever configuration you use


## Factory Reset & Pairing
This bit took me a while...

- Step 1: Put your Zigbee Controller into Pairing Mode
- Step 2: Press the reset button (I used a sim-door key) for 10 seconds
- Step 3: The Light should flash Red & Green constantly
- Step 4: Your Controller should find the device

If the controller struggles to find the device:

- Press and hold all buttons for about 4 seconds and the controller should restart and it might then go into pairing mode
- Failing that, redo the above steps and hold the reset button for a touch longer

## My Current Configuration
!!! important "Automations"
    Automations are the method I've used to configure this device. There are various blueprints on the Home Assistant Community Forums, but I'm content with Automations for now

!!! tip
    Keep it easily searchable by appending all Automations with the same name i.e. I've used "Hue Dimmer". I can then search and alter these as required

### Hue Dimmer Off Button
**Trigger:** Turn Off Button Pressed
**Conditions:** None
**Actions:** Acviate Scene: Bedroom Lights Off

**Role** Simple Automation to Turn off all Bedroom Lights when the "Off" button is pressed on the Hue Dimmer Controller

### Hue Dimmer Double off Button
**Trigger:** Turn Off Button Double Pressed
**Conditions:** None
**Actions:** Activate Scene: Bedroom Lights Off
Choose Condition:

- If the time is after 6:45am and before 11:30am
- AND The Day is a Weekday
- AND the Bedroom Speaker is playing (Assumed Radio 1 due to alarm using this radio station)

THEN:

- Play Radio 1 In the Kitchen
- Stop the media playing in the bedroom

**Role** Automation to allow the usual lights to be turned off, but also transfer the music (Assumed Radio 1) from the Bedroom to the likely next room of the Kitchen 