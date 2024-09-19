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
2. [ ] 2. Once all equipment is gathered make sure to plug the cables into a switch
- make sure that the cables are plugged into the appropriate spots
- make sure that the cables are plugged in all the way
- make sure that the switch is on
3. [ ] 3. Add a Router
  - When adding a router the port status is off by default, make sure that you turn it on for each port being use
     - Commands to turn on Router...
          - config #interface gigabitethernet0/0
          - config # no shutdown
4. [ ] 4. Once all the physical things are set up it is time to set up the systems
   - To set the Default Gateway, go to the end devices and config then type in 

###  3. Frequently Asked Questions
5 Key Questions and Answers
1. haha
   - hello
2. haha 
   - this is 
4. asdf
   - hello
5. asdf
   - hello
6. asdf
   - jello

###  4. Retrospective
Initially, when we started with the fundamentals of networking I was overwhelmed because I did not think I would be able to remember all of the steps. As we have practiced with networks by drawing diagrams, through simulations like Cisco Packet Tracer, and lastly through physically putting together a network with our own devices I have gained a lot more comfortable with the material. Throughout each methodology there were different challenges posed. When we started simply drawing the LANs to make a WAN, I more caught up trying to remember what everything was named and what their primary role or function each device provided to the LAN. Since this was my first encounter thinking about networks I felt like there was a lot of moving parts and struggled grasping the application of this in the real world. As we moved onto the online simulation, I was able to develop a stronger understanding of what each item does and see more of the process of putting together a network. It had more of a hands on approach because you had to turn things on and off, "plug" cables into different devices, and set IP addresses. Since it is a simulation its default is that it is the most ideal set-up because everything is always going to work, unless there was any human error. I noticed throughout the simulation we didn't run into the same problems that we ran into when physically putting together our network in class. I found that I struggled mostly staying on track during class, sometimes it would move really fast and it was very easy to fall behind, especially when trying to take handwritten notes. Although sitting next to someone else and asking for help is always super easy to do in this class. There is a lot of encouragement to troubleshoot your own issues in a variety of ways outside of just asking the professor for assistance, which I appreciate as a student. Lastly, for the physical set up of the LAN and the WAN. This was the most challenging of all the other methods teaching us how to set up a network. This lab just had a lot more room for error and needed to put togehter all the concepts that we learned from the previous weeks together into practice. Through this hands-on-experience I was able to learn a lot and it reminded me of the smaller aspects to troubleshoot. For instance, my group and I ran into a problem where we couldn't ping one end device to another while on the same network. We were thinking of all the possible ways it could ahve gone wrong and were stumped as we double checked everything. As we were still thinking about the potential issues we realized that we never turned on the router, so that is why the end devices could not communicate with one anohter. In both the simulation and drawing activies this was not an experience we could have learned about until we were setting up a network manually. It was the simple things that we overlooked, but they are as equally as important to the process just like everything else to get a network up and running properly. Throughout each methodology I was able to learn many different crucical aspects of networks which has provided me with plenty of examples where networks can fail. This hones on my troubleshooting skills and think of potential reasons for failure depending on the issue at hand. This allows me to make better educated guesses about what is failing in the system to solve problems faster. 

I personally like to take handwritten notes because I think it helps with my understanding and learning of the material covered in class. In some of my classes in the past professors have made fill in the blank worksheets which might be helpful, so it goes by a little faster than waiting for all students to write down their notes. It also gets students writing and mroe engageed with the material without taking too much of the time in class because you are not waiting for all students to write down entire sentences. I would like to see a bigger incorporation of notetaking in class. As I am studying for the interview now, I have been taking notes about things that I want to say and highlight throughout, in order to better retain the material and have it by muscle memory. 




















