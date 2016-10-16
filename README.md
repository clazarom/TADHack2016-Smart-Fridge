# TADHack2016 - Little Endian's Kitchen

Repository for the source code of our Hack during the 14-15 October 2016 Hackathon

Sponsors:
- Telestax https://telestax.com/ 
- Matrix

# Short description

A smart kitche node with a smart fridge. This functions objective is to:
- Detect and have a list of the ingredents that are needed. Either because the fridge is empty or because one resident of the house request them. Users can choose to buy any ingredient, causing said ingredient to be removed from the list.
- Maintain an organize weekly schedule with the house cleaning responsibilites, to be share with all the members of the house
- Include a Virtual Reality demo to display the list of missing ingredents. It can also be used to display the fridge itself and its content

# Components

Raspberry Pi B+ Code - a JS Node displaying the main GUI including Telestax functions
Matrix clients interaction - JS Node maintaining the list of missing ingredents in one of Matrix chat rooms
Virtual Reality server 
