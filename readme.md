# Network Tariff Card

![Network Tariff Card](https://example.com/image.png)

A custom card for Home Assistant that visually displays the current electricity tariff block in a circled 24-hour clock format. This card allows customization of colors for different tariff blocks and offers the option to show or hide the hour labels.

## Features

- **Current Tariff Block**: Displays the current electricity tariff block based on your Home Assistant sensor.
- **24-Hour Clock Format**: Visual representation of the tariff blocks in a circular layout.
- **Customizable Colors**: Set different colors for each tariff block to easily distinguish between them.
- **Toggle Hour Labels**: Option to show or hide hour text for a cleaner design.

## Installation

### Prerequisites

Ensure you have [HACS](https://hacs.xyz/) installed in your Home Assistant.

### Important Note

Please ensure you are using the latest version of the custom component **[Home Assistant Network Tariff](https://github.com/frlequ/home-assistant-network-tariff)**. This card is designed to work with this component.

### Steps

1. **Add Repository**:
   - Go to HACS in Home Assistant.
   - Click on "Frontend."
   - Click on the "+" icon in the bottom right corner.
   - Search for `Network Tariff Card` or add the repository URL directly.

2. **Install**: Click on the repository and follow the prompts to install the card.

3. **Add to Lovelace UI**:
   - Go to your Lovelace dashboard.
   - Click on the three-dot menu (top right) and select "Edit Dashboard."
   - Click on "Add Card" and choose "Manual."
   - Use the following configuration:

   ```yaml
   type: custom:network-tariff-card
   entity: sensor.elektro_network_tariff
   show_hours: true  # Set to false to hide hour labels
   colors:
     - block1: "#FF0000"  # Color for tariff block 1
     - block2: "#00FF00"  # Color for tariff block 2
     - block3: "#0000FF"  # Color for tariff block 3
     - block4: "#FFFF00"  # Color for tariff block 4
     - block5: "#FF00FF"  # Color for tariff block 5
