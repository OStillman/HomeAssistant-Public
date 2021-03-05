# Configuration.yaml
The Configuration.yaml is a really important part of Home Assistant. You'll find yourself avoiding it initially, then using it loads once you get going

!!! info "Split it out!"
    I've fallen into this trap but please, split out your configuration.yaml file. It really will save so much pain!

## How to use the configuration.yaml file
Home Assitant takes you through some really useful tutorials, but it does really depend on your use case. Lots of documentation will jump straight into some .yaml when there is actually a UI configuration availiable. And generally, use the UI Configuration if you can, it avoids so much annoyances!

Generally there are a few small rules:

- Make small Changes
- Check Configuration (Configuration > Server Controls > Check Configuration)
- Restart after most, if not all, changes to see them take effect
- Make use of the [secrets.yaml file](https://www.home-assistant.io/docs/configuration/secrets/)
- Make use of [splitting out the config file](https://www.home-assistant.io/docs/configuration/splitting_configuration/)

!!! tip "My Configuration"
    In the Nav structure you'll see how I've configured my yaml files. My main file is described below, and I've mirrored the directory structure in here to make it easy for me to revert to if I need to check anything. You can however sort yours in anyway you deem best!