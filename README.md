# ISBA 4775: Cloud Computing and Networking

## Mini Project 01

September 18, 2024


Cleo Pollinger

###  1. System Architecture Diagram

<img width="701" alt="Screenshot 2024-09-18 at 11 34 17 PM" src="https://github.com/user-attachments/assets/54b7c4dd-defc-4d7b-99ca-0f4025d8ed62">

This is a system architecture diagram that we conducted while in class. We based it off of the ISBA lounge and the Data Center in UHall. In the ISBA lounge there are tons of desktops as the end devices, which I presume are connected to a switch and all hooked to a router. This router is also connected to the data center in UHall, which has end devices of servers. These servers are similarly connected to a switch just like the desktops in the ISBA lounge. This switch is also connected to the router. This diagram shows the physical set up of all devices but not the nitty gritty bits setting up these devices. Assuming that all of the smaller details were set up properly it allows devices from the ISBA Lounge to communicate to servers at the Data Center in UHall. This is how we made a Wide Area Network (WAN) composed of two smaller Local Area Networks (LAN).

<img width="846" alt="Screenshot 2024-09-18 at 10 20 57 PM" src="https://github.com/user-attachments/assets/1b31d471-e2f2-4b09-bdc5-e14c94a49c1b">

This is a System Architecture Diagram based off of our lab in class. I used the same methodology that we learned in class to apply my learning to a real world example. I incorporated an example from my personal life. I used my Dad's home office for a reference and my Brother's room. My Dad's office is located right next to my Brother's room, which is convenient for both parties because the wiring isn't too far apart from each person's end devices. I used desktop PCs as end devices wired to switches and connected to the same router. I am pretty sure this is how it is physically set up in my house, but not accurate to the IP addresses or types of hardware.

###  2. Step-by-Step Configuration Guide
When setting up a basic Wide Area Network (WAN) these are a few guiding steps to help ensure it works properly.

1. [ ] 1. Gather all necessary equipment and materials 
   - set it up
   - make sure things are plugged in and working properly
2. [ ]  2. Once all equipment is gathered make sure to plug the cables into a switch [ ]
- make sure that the cables are plugged into the appropriate spots
- make sure that the cables are plugged in all the way
- make sure that the switch is on
3. [ ] 3. Add a Router [ ]
  - When adding a router the port status is off by default, make sure that you turn it on for each port being use
     - Commands to turn on Router...
          - config #interface gigabitethernet0/0
          - config # no shutdown
4. [ ] 4. Once all the physical things are set up it is time to set up the [ ]

###  3. Frequently Asked Questions

###  4. Retrospective
