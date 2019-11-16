# command-line-compass
Ubuntu Touch @UBports based cl compass. Tested on BQ Aquaris E4.5 aka "kirillin". It is running in my version of atlast Forth. https://github.com/skvamme/atlast Compile atlast on a raspberry pi and copy over to phablet directory on the mobile using e.g. scp

If you are new to Forth I recommend reading this great book by Leo Brodie https://www.forth.com/starting-forth/0-starting-forth/

The compass has man overboard functionality. Current location can be saved and later you can get distance and bearing to that saved place. It works equally well when you are "lost in town" and want to get back to your hotel. No maps required.

Start the terminal app and start atlast with sudo ./atlast -icompass.atl Stop atlast with Ctrl-D

Usefull words are:
  init for calibration.
  run for compass.
  Both these words run until stopped with Ctrl-C. Just type the word and press Enter. When you run init you should move in all compass directions until no more changes are visible in xmax, ymax ...
  
  save for saving the current location.
  ber for getting bearing to saved position.
  dist for getting distance to saved position.
  For these three words to be able to pick current gps location, type the word and switch over to the weather app or a map for a minute or so. These apps are activating the gps while visible so the compass can grab lat and long readings and do all calculations in the background.
  
  When you switch back to the terminal app it says that the app is stopped. Type fg to get it back in foreground again.
  
You will see lots of 0 and -1, and at end of last line is the result. 0 and -1 are for debugging.

The word send-sms can be used to send current location, saved location or other message as an SMS. The word smspos grabs current lat and long and sends that as an SMS. To let the compass grab the current position, switch over to the weather app or a map for a minute. The GPS icon in the top screen should light up. Replace the dummy phone number with a valid one in the file compass.atl or if you want to change the number temporarily you can redefine the word smsto in the running atlast: Type : smsto "the_number_here" ;  Mind the spaces. Atlast will always use the latest definition of the word smsto. And forget all of them when you switch of.
