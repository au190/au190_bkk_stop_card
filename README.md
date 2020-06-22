# Lovelace custom card for BKK Stop Information

This Lovelace custom card displays Budapest Public Transportation (BKK)
line information departing in the near future from a configurable stop.<p>
This custom card depends on the BKK Stop Information custom component that you may find at
https://github.com/au190/au190_bkk_stop


#### Installation
The easiest way to install it is through [HACS (Home Assistant Community Store)](https://custom-components.github.io/hacs/),
search for <i>bkk</i> and select BKK Stop Card from Plugins.<br />
If you are not using HACS, you may download bkk_stop_card.js and put it into $homeassistant_config_dir/www/community/<br />

#### Lovelace UI configuration
Add the following lines to your ui-lovelace.yaml (entity should be the sensor of bkk_stop platform you defined):
```
resources:
  - {type: module, url: '/www/community/au190_bkk_stop_card/au190_bkk_stop_card.js '}

cards:
  - entity: sensor.99_home_city
    type: 'custom:bkk-stop-card'
  - entity: sensor.99_vajdapeter_home
    type: 'custom:bkk-stop-card'
  - entity: sensor.99_blaha_home
    type: 'custom:bkk-stop-card'
  - entity: sensor.99_tess_home
    type: 'custom:bkk-stop-card'
  - entity: sensor.23_boraros_home
    type: 'custom:bkk-stop-card'
  - entity: sensor.23_home_city
    type: 'custom:bkk-stop-card'
type: vertical-stack
```

Lovelace UI:<br />
<img src='https://raw.githubusercontent.com/au190/au190_bkk_stop_card/master/bkk_lovelace.png'/>


Updated server side
Updated client side (shows when was updated)
Original: https://github.com/amaximus/bkk-stop-card