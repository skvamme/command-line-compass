# command-line-compass
Ubuntu Touch @UBports based cl compass. It is running in my version of atlast. https://github.com/skvamme/atlast Compile atlast on a raspberry pi and copy over to phablet directory on the mobile using e. g. scp

The compass has man overboard functionality. Current location can be saved and later you can get distance and bearing to that saved place.

Start the terminal app and start atlast with sudo ./atlast -icompass.atl

Usefull words are:
  init for calibration.
  run for compass.
  Both these words run until stopped with Ctrl-C
  
  save for saving the current location.
  ber for getting bearing to saved position.
  dist for getting distance to saved position.
  For these three words to be able to pick current gps location, type e.g. save and switch over to the weather app or a map for a minute or so. These apps are activating the gps while visible so the compass can grab lat and long readings and do all calculations in the background.
  
  When you switch back to the terminal app it says that the app is stopped. Type fg and the enter key a few times to get it back in foreground again.
  
You will see lots of 0 and -1, and at end of last line is the result. 0 and -1 are for debugging.

The word send-sms can be used to send current location, saved location or other message as an SMS.
