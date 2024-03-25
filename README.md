<!-- ![logo](images/logo.png) -->
<div style="text-align: center">
    <img src="images/logo.png" alt="Digo Technology Jsc">
</div>

The Digo Bridge integration allows you to make your Home Assistant entities available in Digo platform, so they can be controlled by Digo Smart app; even if those devices are not produced by Digo.

# Installation

For manual installation, copy the digobridge folder and all of its contents into your Home Assistant's custom_components folder. This folder is normaly inside your `/config` folder. If you are running Hass.io, use SAMBA to copy the folder over. If you are running Home Assistant Supervised, the custom_components folder might be located at `/usr/share/hassio/homeassistant`. You may need to create the `custom_components` folder and then copy the digobridge folder and all of its contents into it.


# Adding the Integration
To start configuring the integration, just press the "+ADD INTEGRATION" button in the Settings - Integrations page, and select Digo Bridge from the drop-down menu.

After pressing the Submit button, the Integration will be added. The entities are exposed to Digo Smart if they are supported. To add them:

* Open the Home Assistant frontend. A new card will display the pairing QR code as seen in the example below. Note: If QR code is not displayed, check “Notifications” (the bell icon) in the lower-left of the Home Assistant UI.
* Open the Digo Smart app.
* Click Add device, then scan the QR code
* Follow the setup by clicking on Next and lastly Done in the top right-hand corner.

After the setup is completed, you should be able to control your Home Assistant integrations through Digo Smart App.
# Debugging

Whenever you write a bug report, it helps tremendously if you indicate sufficient debug logs directly (otherwise we will just ask for them and it will take longer). So please enable debug logs like this and include them in your issue:

```yaml
logger:
  default: warning
  logs:
    custom_components.digobridge: debug
```
