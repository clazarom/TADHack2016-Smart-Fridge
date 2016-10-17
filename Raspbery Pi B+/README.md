# Raspberry Pi B+ - JS Node

The Raspbery Pi is the house fridge interface. We implemented a JS Node to work as the inhouse interaction with our services. At this point the node is capable of:
- Show a list of current missing ingredients
- Show a lit of the week's cleaning duties. This list is to be updated every Monday (in the code, we inclue an "It's Monday" button to emulate the beginint of a new week), and will:
      - Assign each person to a new task in an orderly manner
      - Send an email to all the residents (using Telestax)
- Include some sample Telestax function: a send message dialog and call/hangup buttons

# Requriements
  To run any of the WebRTC capabilites (and well... the project itself), you need to have a Telestax account (https://tadhack.restcomm.com/#/login). In this account we have configured the:
  - Users and their passwords.
  - Clients (with their number).
  - Projects to respond to the Raspberry Pi actions
  
  We are using the host provided during the Hackathon - tadhack.restcomm.com 
  
  Here are we can configure different WebRTC applciations/projects, which will determine what happens when a certain user calls, a call to a client is received, or a message to a client is received.  The Raspi will setup a user and send calls/messages to a client, and the projecs in Telestax responding to this actions will be sending the actual emails/SMS/Calls to the residents.
  
  NOTE: With Telestax youc an also configure your own local server, though we are hosted in their cloud 

# How to run the project
  In /www we launch the server.js node: $nodejs server.js 
  (There is the option of running also a secure version of this server, serving HTTPS, launching server-secure.js: $nodejs server-secure.js)
  
  We can now open a browser in the same computer to access the Pi JS Node. Server.js is serving at port 7080
  http://localhost:7080/
  (For server secure: https://localhost:7443/)
  
  It can also be acccessed by other machines in the net, using the PI local address:
  http://local_ip:7080
  
  Furthermore, we installed a Apache web server in the Pi (though we have to work a few things to include a proper remote access)

# More about Telestax
  Telestax includes very complete tutorials, SDKs and sample projects. 
  Some interesting links to their video tutorials:
  https://telestax.com/design-package-and-submit-an-application-to-restcomm-app-store-in-less-than-5-minutes/
  http://documentation.telestax.com/connect/rvd/Restcomm%20-%20RVD%20Quick%20Video%20Tutorial.html#building-the-apps
  
  We started at one of the links provided during the Hackathon, and based this part of the hack in their Restcomm JavaScript  WebRTC
  http://documentation.telestax.com/connect/sdks/restcomm-client-web-sdk-quick-start.html#web-sdk-guide
  

