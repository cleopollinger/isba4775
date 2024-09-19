# ISBA 4775: Cloud Computing and Networking

## Mini Project 01

September 19, 2024


Cleo Pollinger

###  1. System Architecture Diagram

<img width="701" alt="Screenshot 2024-09-18 at 11 34 17 PM" src="https://github.com/user-attachments/assets/54b7c4dd-defc-4d7b-99ca-0f4025d8ed62">

[System_Architecture_Diagram.pdf](https://github.com/user-attachments/files/17060047/System_Architecture_Diagram.pdf)


This is a system architecture diagram that we conducted while in class. We based it off of the ISBA lounge and the Data Center in UHall. In the ISBA lounge there are tons of desktops as the end devices, which I presume are connected to a switch and all hooked to a router. This router is also connected to the data center in UHall, which has end devices of servers. These servers are similarly connected to a switch just like the desktops in the ISBA lounge. This switch is also connected to the router. This diagram shows the physical set up of all devices but not the nitty gritty bits setting up these devices. Assuming that all of the smaller details were set up properly it allows devices from the ISBA Lounge to communicate to servers at the Data Center in UHall. This is how we made a Wide Area Network (WAN) composed of two smaller Local Area Networks (LAN).

<img width="846" alt="Screenshot 2024-09-18 at 10 20 57 PM" src="https://github.com/user-attachments/assets/1b31d471-e2f2-4b09-bdc5-e14c94a49c1b">

[System_Architecture_Diagram_2.pdf](https://github.com/user-attachments/files/17060123/System_Architecture_Diagram_2.pdf)

This is a System Architecture Diagram based off of our lab in class. I used the same methodology that we learned in class to apply my learning to a real world example. I incorporated an example from my personal life. I used my Dad's home office for a reference and my Brother's room. My Dad's office is located right next to my Brother's room, which is convenient for both parties because the wiring isn't too far apart from each person's end devices. I used desktop PCs as end devices wired to switches and connected to the same router. I am pretty sure this is how it is physically set up in my house, but not accurate to the IP addresses or types of hardware.

###  2. Step-by-Step Configuration Guide
**OBJECTIVE: To set up a basic network using wired end devices, without a modem.**

Setting up a basic network is essential, and there are many variations in how home networks can be configured. In this guide, we will focus on connecting wired end devices with Ethernet cables. Keep in mind that home networks can also include wireless connections and modems, but these are not covered here.

Some common use cases for a network include:
- Two people playing video games together from their respective homes
- Two people holding a Zoom meeting from their home offices
- Using a remote support chat box for troubleshooting or assitance

When setting up a basic Wide Area Network (WAN), follow these steps to ensure proper set-up:

1. [ ] 1. Gather All Necessary Equipment and Materials
<img width="778" alt="Screenshot 2024-09-19 at 9 59 22 AM" src="https://github.com/user-attachments/assets/44a35871-ccc9-456d-9587-ccd5f306a223">

*Cisco Packet Tracer doesn't allow you to represent loose cords, but you should have ethernet cords out*

 - set up your end devices (PCs, MacBooks, Printers, etc.)
 - make sure things are plugged in with ethernet cables and working properly
 - turn on all devices and hardware, such as the Router and Switch. The switch and router needs to be plugged into a socket.
<img width="459" alt="Screenshot 2024-09-19 at 10 03 11 AM" src="https://github.com/user-attachments/assets/78aca9a5-8eaa-4095-a685-d79d8f5045a1">

*Router plugged into socket and turned on*

<img width="459" alt="Screenshot 2024-09-19 at 10 03 49 AM" src="https://github.com/user-attachments/assets/54d5da41-2170-450d-a47c-b633a757406b">

*Switch plugged into socket*

2. [ ] 2. Connect Devices to the Switch
- Plug the ethernet cables from the end devices to the switch
 - make sure that the cables are plugged in all the way
 - make sure the cables are plugged into the correct ports on the switch
 - make sure the switch is on

<img width="688" alt="Screenshot 2024-09-19 at 10 06 35 AM" src="https://github.com/user-attachments/assets/163f0a0e-be2f-4aa1-b5e8-1b9a6b762099">

*the ethernet cables have been plugged in from end devices to switch*

3. [ ] 3. Configure the Router
  - Connect the Router to the Switch using ethernet cables

<img width="688" alt="Screenshot 2024-09-19 at 10 08 18 AM" src="https://github.com/user-attachments/assets/37bb8f51-616e-46a8-b1ad-46c997bc2d11">

*Prior to turning on the router ports, so connection is not set up yet. Only added the ethernet cables from switch to router*

  - When adding a router the port status is off by default, make sure that you turn it on for each port being used
     - Commands to turn on Router...
       ```
       config # interface gigabitethernet0/0
       config # no shutdown

       ```
       *the numbers from this command "gigabitethernet0/0" will change depending on the port number, so be mindful when turning on Router ports*

<img width="675" alt="Screenshot 2024-09-19 at 10 09 52 AM" src="https://github.com/user-attachments/assets/6887234f-de76-4e77-980c-25de6dc773e1">

*From this image you can see that the port status is on and that the commands have been called to turn on the router port*
 
4. [ ] 4. Configure IP Addresses and Gateways

Once all the physical things are set up it is time to set up the systems...

- Set up IP Addresses on all end devices, in this case since it is a home network we are going to use private Class C IP Addresses. For the example above we set the IP Address to be 192.168.0.2-192.168.0.245, you can use any of these IP addresses but be sure to properly label and keep track of what devices are attached to specific IP addresses.



<img width="693" alt="Screenshot 2024-09-19 at 10 14 37 AM" src="https://github.com/user-attachments/assets/1c1fdc61-d4b4-4224-b4ec-cb6aff174d0d">

*Setting up the IP Address and Subnet Mask on the PC*

- Set up IP address on router, typically routers are the first IP Address in the set. So in this case the router's IP address would be 192.168.0.1 on the left-hand side LAN.


<img width="693" alt="Screenshot 2024-09-19 at 10 17 47 AM" src="https://github.com/user-attachments/assets/ac4cba0b-9de8-4fff-8408-343ca8b3468a">

*IP address set up on router with subnet mask and the corresponding commmands, be sure to set the IP address for every port. This was for port 0/0*

<img width="670" alt="Screenshot 2024-09-19 at 10 19 21 AM" src="https://github.com/user-attachments/assets/f0459e77-2127-4ee3-9534-05baadc51c0d">

*IP address and subnet mask set up for port 0/1*

- Lastly, set the Default Gateway, go to the end devices and config then type in the router's IP Address, make sure to do this for every port being used.
  - Since we have two LANs in this scenario the ISBA LAN is going to have a default gateway set to 192.168.0.1

<img width="670" alt="Screenshot 2024-09-19 at 10 21 21 AM" src="https://github.com/user-attachments/assets/b932498f-f161-45fd-9a05-dd7dbeb55b32">

*This is set up through the end-devices*

  - The Data Center LAN to the router will have a default gateway set to 172.16.0.1 and the subnet mask is 255.255.255.0
 
 <img width="670" alt="Screenshot 2024-09-19 at 10 25 20 AM" src="https://github.com/user-attachments/assets/481e00d3-3427-48f0-af8b-74b6942f8af6">

*This is the set up of the default gateway from the right hand side of the router*

***END RESULT***

<img width="747" alt="Screenshot 2024-09-19 at 10 26 52 AM" src="https://github.com/user-attachments/assets/f7104b83-1120-4629-baee-d7240467f8a3">

Congratulations, you have just set up a basic network! 

###  3. Frequently Asked Questions
Key Questions and Answers to address commmon issues and provide clear solutions for creating, modifying, or maintaining the system. 


**1. What equipment do I need to set up a basic home network?**
   - Answer: The equipment needed to set up a basic home network would be an end device, ethernet cables, a switch, and a router. For the most part in basic home networks they incorporate combination devices that are both routers and switches in one device. This helps minimize user error and provides an easier set up for individuals. If you have a combination device it is still important to have ethernet cables to plug devices like a printer, desktops, or even a smart TV.

     
**2. What's the difference between a router and a switch?**
   - Answer: A router helps send the necessary data to the correct location and distribute the internet connection to end devices, whereas a switch helps connect end devices together on the same local area network to communicate with one another. Routers are more important for across local area networks also known as a wide area network.

     
**3. What is a Modem? Do I need one for my basic home network?**
   - Answer: A modem is a device that connects your home network to the internet through an Internet Service Provider (ISP). It depends, sometimes you will need a modem depending on how you are planning to access the internet. Some examples of when you will need a modem is when you are using cable, DSL, or fiber internet. This guide was under the assumption that you are creating a network based on ethernet, so we did not have to incorporate a modem into our diagram and instructions. The ethernet cables are directly connected to an ISP, which would allow the router to connect directly to internet provided.

     
**4. How do I know if my devices are properly connected to the network?**
   - Answer: One way to discover if your devices are properly connected to the network is through your end devices terminals. Through the terminal you can PING another end device by the command "PING {INSERT IP Address}." This will run a command to check to see if there is another end device on the network. Another way to check is through the physical connections of the ethernet cables for these end devices.

     
**5. Why is my internet connection slow? What should I do to fix it?**
   - Answer: There might be multiple reasons why your internet connection is slow. One potential issue is the placement of your router. If your router is not in a centrally located area and blocked by many objects it could slow down the wireless connection for end devices. Another potential issue might be the network having too many devices on it which is slowing down the connection to your device. By having multiple devices on the same network it will cause the network to get congested which will slow down internet speed. One way to fix it is to implement another network and offload some of the devices onto another point of connection. Another way is to set up Quality of Service (QoS) on your router which would prioritize specific activities on the network over others. Lastly, you might have old hardware or devices that might be slowing down your internet connection. By updating or upgrading your devices and or hardware it ensures the most up to date quality and performance. This can help with internet speeds. There are plenty more reasons for slow internet connection, but these are some of the main reasons.

     
**6. What is a firewall? Do I need one for my network?**
   - Answer: A firewall is an added security measure to monitor and control incoming and outgoing network traffic. Modern routers have firewalls built into them in order to have basic protection against any threats, so it might not be an issue for current devices. Although, it is still a good idea to check and see if your router has a firewall built-in or not. Having a firewall is not a necessary component of a network, but it is a good idea to enable one in order to prevent unauthorized access to your network, if your router does not have one already built in. 

###  4. Retrospective
*Introduction*

Initially, when we started with the fundamentals of networking I was overwhelmed because I did not think I would be able to remember all of the steps. As we have practiced with networks by drawing diagrams, through simulations like Cisco Packet Tracer, and lastly through physically putting together a network with our own devices. I have gained more comfortability with the material because of the different types of practice we had. Throughout each methodology there were different challenges posed. 

*Drawing a Network*

When we started simply drawing the LANs to make a WAN, I more caught up trying to remember what everything was named and what their primary role or function each device provided to the LAN. Since this was my first encounter thinking about networks I felt like there was a lot of moving parts and struggled grasping the application of this in the real world. 

*Cisco Packet Tracer*

As we moved onto the online simulation, I was able to develop a stronger understanding of what each item does and see more of the process of putting together a network. It had more of a hands on approach because you had to turn things on and off, "plug" cables into different devices, and set IP addresses. Since it is a simulation its default is that it is the most ideal set-up because everything is always going to work, unless there was any human error. I noticed throughout the simulation we didn't run into the same problems that we ran into when physically putting together our network in class. I found that I struggled mostly staying on track during class, sometimes it would move really fast and it was very easy to fall behind, especially when trying to take handwritten notes. Although sitting next to someone else and asking for help is always super easy to do in this class. There is a lot of encouragement to troubleshoot your own issues in a variety of ways outside of just asking the professor for assistance, which I appreciate as a student. 

*Hands-on Network Building*

Lastly, for the physical set up of the LAN and the WAN. This was the most challenging of all the other methods teaching us how to set up a network. This lab just had a lot more room for error and needed to put togehter all the concepts that we learned from the previous weeks together into practice. Through this hands-on-experience I was able to learn a lot and it reminded me of the smaller aspects to troubleshoot. For instance, my group and I ran into a problem where we couldn't ping one end device to another while on the same network. We were thinking of all the possible ways it could ahve gone wrong and were stumped as we double checked everything. As we were still thinking about the potential issues we realized that we never turned on the router, so that is why the end devices could not communicate with one anohter. 

*Overall Learning*

In both the simulation and drawing activies this was not an experience we could have learned about until we were setting up a network manually. It was the simple things that we overlooked, but they are as equally as important to the process just like everything else to get a network up and running properly. Throughout each methodology I was able to learn many different crucical aspects of networks which has provided me with plenty of examples where networks can fail. This hones on my troubleshooting skills and think of potential reasons for failure depending on the issue at hand. This allows me to make better educated guesses about what is failing in the system to solve problems faster. 

*Future Changes*

I personally like to take handwritten notes because I think it helps with my understanding and learning of the material covered in class. In some of my classes in the past professors have made fill in the blank worksheets which might be helpful, so it goes by a little faster than waiting for all students to write down their notes. It also gets students writing and mroe engageed with the material without taking too much of the time in class because you are not waiting for all students to write down entire sentences. I would like to see a bigger incorporation of notetaking in class. As I am studying for the interview now, I have been taking notes about things that I want to say and highlight throughout, in order to better retain the material and have it by muscle memory. 

