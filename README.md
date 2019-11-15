# command-line-compass
Ubuntu Touch @UBports based cl compass. It is running in my version of atlast. Compile atlast on a raspberry pi and copy over to phablet directory on the mobile using e. g. scp

The compass has man overboard functionality. Current location can be saved and later get distance and bearing to that saved place.

Usefull words are:
  init for calibration.
  run for compass.
  Both these words run until stopped with Ctrl-C
  
  save for saving the current location.
  ber for getting bearing to saved position.
  dist for getting distance to saved position.
  For these three words to be able to pick current gps location, type e.g. save and switch over to the weather app or a map for a minute or so. These apps are activating the gps while visible so the compass can grab lat and long readings in the background.
