---
layout: portfolio_entry
title: Guy Walks into a Apple Store Looking to Buy an iBeacon -> What are iBeacons?
tags:
  - iBeacon
  - invention
  - marketing
---

So I went into an Apple Store and asked one of the geniuses "Do you have any iBeacons in stock?"

More specifically right before going into a Sonic Notify board meeting, at the amazing [Raptor Venture](http://www.raptorventures.com/ "Raptor") offices. I went into the Apple store right below and asked.

<div align="center"><iframe width="640" height="480" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="https://www.google.com/maps?f=q&amp;source=s_q&amp;hl=en&amp;geocode=&amp;q=Raptor+Capital+Management&amp;sll=40.740504,-74.005076&amp;sspn=0.002667,0.004128&amp;t=h&amp;ie=UTF8&amp;hq=Raptor+Capital+Management&amp;hnear=&amp;ll=40.741345,-74.00552&amp;spn=0.00069,0.000858&amp;z=20&amp;output=embed"></iframe><br /><small><a href="https://www.google.com/maps?f=q&amp;source=embed&amp;hl=en&amp;geocode=&amp;q=Raptor+Capital+Management&amp;sll=40.740504,-74.005076&amp;sspn=0.002667,0.004128&amp;t=h&amp;ie=UTF8&amp;hq=Raptor+Capital+Management&amp;hnear=&amp;ll=40.741345,-74.00552&amp;spn=0.00069,0.000858&amp;z=20" style="color:#0000FF;text-align:left">View Larger Map</a></small></div>

> Me:  Do you have any iBeacons in stock?
>
> Genius: What is an iBeacon? Is that an accessory? 
>
> Me: Here is a picture from a WWDC talk in which a beacon device sends a message to a phone in a doughnut shop. 
> 
> Genius: I could check in the back. But unless its a weird accessory I dont think we sell them. 
>
> Me: Ok, when someone complains about bad battery life, what do you tell them to do?
>
> Genius: Turn off bluetooth, wifi, movement, and anything else you aren't using. 
>
>Me: Thanks

##What the hell is an iBeacon?

On sales calls, meetups, and talking to my mother I get a lot of different questions about what iBeacons are. The general consensus is that its a device that is used to show marketing to users when they are close to the object. I.e. You will walk into a store and your phone will buzz and say "Do you want coffee?"
![Alt text]({{ site.url }}/img/posts/beaconsSuit.png)

[Iggymwangi](http://en.wikipedia.org/w/index.php?title=IBeacon&diff=581491577&oldid=581452824) wrote on wikipedia that iBeacons are "in a single sentence is a technology that enables an iDevice or other hardware to send push notifications to iDevices within close proximity."

I disagree, iBeacons dont present marketing, "iBeacons" are marketing. 

**iBeacon is a marketing term created by Apple in order to brand a software api callback added into the location managment software in the iOS SDK so that software applications can register for callbacks when the phone comes in proximity to a bluetooth signal matching the developers identifier.**

### Questions about iBeacons, think Apple Push Notification Services
Maybe to explain iBeacons it is helpful to think about Push Notifications on a iOS device. What are Push Notifications? And how are they different than the Apple Push Notification Service? And how is that different than "your phone will buzz in your pocket when your friend sends you a snapchat." 

Problem: Someone sends a snapchat to a user, but the users app is closed/background etc. </br>
SimpleSolution: Developer keeps their app running in the background forever and opens a http socket to a server. New message comes in via HTTP request and the developer buzzes the phone etc. The problem of course is 

* Apple doesnt let phones run in the background forever
* May not be super great to have all these apps remainging in the background with open connections </br>
</br>
RealSolution:Apple comes to the rescue and provides a mechanism for your server to send a message to Apple's server, which sends a message to a piece of software in the operating system which is "listening" for incoming calls and delivers the message. 
</br>
![Alt text]({{ site.url }}/img/posts/iphone-push-notification-service-arch.jpg)
###### Apple Push Notifications Work Like This
</br>
iBeacon and proximity beacons are a very similar story. For years companies have been building systems to listen for signals(Bluetooth, Audio, etc) to deliver marketing in proximity. But just like push notification there are problems, can't poll in the background etc. So Apple steps in and adds functions/callbacks in its Location Managment API so that your app can get alerted when you are near a device. What revoulionary technology is Apple doing in the operating system? Same thing people were doing for years, they are just doing it across apps and with optimizations, because they can, they wrote the operating system.

So bringing it full circle. iBeacon is a marketing term. It means Apple put some software code into the operating system that makes it easier for the app you write to get notified when it comes near bluetooth signals. And you know what, thats pretty awesome. It really does add to the capabilities of app developers when creating apps with proximity needs. Well done Apple. But it doesnt deliver notifications and it doesnt take people to twitter and it wont revolutionize retail, we as developers have to do that. 

##Points to Remember

* iBeacons are software callbacks in an app, i.e. the user needs an app.
* iBeacon callbacks return a number ( or two numbers doesnt really matter, its a single identifier)
	* It doesnt send a notification
	* It doesnt deliver a web page
	* It is a number
* And Apple didnt invent shit, they did what they do best, Marketing.

At Sonic Notify we have been delivering proximity beacon solutions for over 2 years. We have the beacons, but more importantly we are an **enterprise solution to a proximity problem.** When you want to reach 95% of smartphones (iPhones, Androids, and Devices with bluetooth off), when you want a enterprise CMS to manage content, when you want a massive analytics engine for data processing, etc. In short if you are a medium/large business who wants to reach consumers in proximity, there is no better choice than Sonic Notify.
