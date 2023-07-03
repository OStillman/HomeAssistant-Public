# Home Assistant

The "real" reason this server exists. This is the main Home Automation/Control/Dashboard Platform and is System Critical and Crucial to my Home.

## Configuration
  * Docker Installation
  * Contains many configuration files for Dashboards, Services, Scripts etc.

## Use Cases

Home Assistant is the Main Platform, though does not deal with the automations. Node-Red is a more visual platform that makes it easier to create complex automations. Instead, Home Assistant Serves as the:

  * State-Machine - Stores all current states of devices for easy access
  * Service Connector - Connects to all Zigbee devices via Zigbee2MQTT, Smart TVs, Google Assistant, Weather Providers etc.
  * Dashboard - Though not relied upon, quick, simple dashboards for out-of-automation control and quick data views


## Automation Vs. Google Assistant, Vs Dashboard decisions

To decide how a certain service will be called (e.g., light turned on, state changed etc.) I follow the following principles. 

  * Automation Potential - Is there a set time, set action, set goal in which this scene, toggle, etc. is needed? E.g., At (or just before) sunset, turn the house to evening mode, switching on lights etc.
  * (If Not) Google Assistant Requirements - Will this be frequently manually toggled at different times throughout the day? E.g., When it's time to go to sleep, use a goodnight routine to trigger a script to put the house into sleeping mode
  * (If Not) Add it to a dashboard


The majority of switches/toggles/services can be accessed via a dashboard for quick toggling where e.g., it can make more sense to quickly toggle via the app rather than voice command whilst music is being played.

## Known Issues / Current Refinement Goals

  * Fine-tune notification configurations - Too many notifications, data is still useful etc.
  * Away mode notifications

## Backup Strategy
  * Included in Portainer Daily Image
  * Configuration Backup Taken before Software Update or Server Maintenance is undertaken