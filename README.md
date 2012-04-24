LabVIEW Pusher Client
=====================

This is simple pusher client library for LabVIEW. This library is developed in LabVIEW 2009 but it will work fine in later versions as well. 
This client has been developed with native VIs and doesn't have any dependency on external toolkit or packages.

NOTE: This library requires National Instruments [LabVIEW] (http://www.ni.com/labview) 2009 of higher development environment.

Assumptions
------------

Since there is no native JSON parser for LabVIEW, we must stick to known event data format while publishing, for this library to parse
and understand it successfully. The format must be correctly formatted according to JSON. 

The format must be (key value json pairs), like the following format 

`{"sampleRate": "1000", "channel": "1","sampleToRead":"10"}`

Examples
-----------

The library has two reference example VIs. One is intended to run on PC while other on NI RT target.

###Pusher_ClientExample.vi

This VI is mainly designed to be run on the PC. Following the following steps to run it.

* Open the VI
* Fill in your pusher API key that you received from your pusher account.
* Run the LabVIEW VI
* Use "Event Creator" tab on pusher.com website to send events to your channel in the following format

Channel Name:`LvChannel`

Event name:`message`

Event data:`{"name":"joe","age":"30"}`


###Pusher_ClientExample_RT.vi

This VI is main designed for National instruments real time (RT) targets such as [compact RIO] (http://www.ni.com/compactrio/) etc. 
It has been tested on compact RIO controller.



Feedback and improvement suggestions welcomed.

Have fun!

A Paracha