# OneBusAway
This is an expansion of a custom component for Home Assistant created by Spacetech

Support for OneBusAway bus arrival times

Request api key here: http://pugetsound.onebusaway.org/p/ContactUs.action
Find your stop id here: http://pugetsound.onebusaway.org/where/standard

minutes_after - include vehicles arriving or departing in the next n minutes

Example configs:

sensor:
    # for http://pugetsound.onebusaway.org/where/standard/stop.action?id=1_700&route=40_100236
    - platform: onebusaway
      name: Westlake Center
      api_key: !secret onebusaway_api_key
      id: "1_700"
      routes:
        - id: "40_100236"
          name: 545E
      minutes_after: 60

or 
    - platform: onebusaway
      api_key: !secret onebusaway_api_key
      id: "1_701"
