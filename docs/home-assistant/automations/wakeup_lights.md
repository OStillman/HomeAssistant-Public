# Wakeup Lights

!!! question "Status: Newly Implemented"
    This Automation is newly configured. It's likely going to go through changes before it's committed and marked fully working

![Wakeup Light Card in Home Assistant](/assets/images/alarms.png)

## Automation Purpose
This automation takes over the Hue Integration for controlling slow-and-steady wakeup lights in the morning. 

## Prior to Automation
Prior to the automation, this used to run from the Hue app. Although this worked, it lacked the flexibility to easily & quickly update, something the use of this automation will resolve

## Implementation

### Package

This automation is stored in *packages/wakeup_lights.yaml*

### UI / Toggles & Time Inputs
The UI consits of Toggles & Time fields as explained below:

Each Alarm

- (E.g.) input_boolean.weekday_wakeup_lights - Input Boolean to toggle the Weekday Lights Turning on
- (E.g.) input_datetime.weekday_light_time - Input Datetime (Time Only) to set the time the lights should start turning on

!!! note
    This Automation assumes the time set is *half hour before* the user wishes to wake up. I.e. Main Alarm at 6:45am, Lights Turn on Time set to 6:15am

### Automations
Plural! Because we need 1 automation for each input type. I.e. Weekday, Saturday & Sunday

- E.g. Wakeup Lights (Weekday)
  - Trigger:
    - Time = input_boolean.weekday_light_time
  - Condition:
    - input_boolean.weekday_wakeup_lights - is *on*
    - AND
    - It's Monday, Tuesday, Wednesday, Thursday or Friday
  - Action:
    - Call Service Light.turn_on
      - Devices: Both Bedside Lamps
      - Transition: 1800 (Half hour transition)
      - Brightness: 100% (Transition up to 100% over half hour)