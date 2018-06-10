# RaspWakeUp #0 - init()

### what
A couple of years ago, i got myself one of this fancy alarm clocks, that simulate a sunrise some minutes before the actual alarm is triggered. It's pretty good, but since getting up & awake is the worst part of the day for me, i am constantly looking to optimize that experience.

In a nutshell i am building a RaspberryPi powered alarm clock, that fits all my alarm-clock-needs so i will rise & shine every day from now on ;) I will take my time to evalualte software and hardware decisions, so this is just an introduction into a series of posts regarding my RaspWakeUp project.

### windows iot
Being a C# developer for some solid years, i was impressed how easily you can transfer a lot of your existing know-how to IoT development using Windows 10 IoT. Of course there are some ohms and farads involved, but thats part of the challange. Also during the last year people started porting some essential libraries for Windows IoT like [433mhz sender/receiver](https://github.com/michaelosthege/RCSwitch) or [HD44780 displays](https://github.com/ms-iot/TextDisplay), so what's not to like? :)

### features
Software and hardware wise i like to think of the project in separate components. So i can develop (or solder) them one by one. I the meantime i just use mocks. So here is a list of mandatory hardware features the RaspWakeUp should have:

* display (some oldschool dotmatrix lcd)
* speaker
* volume control
* buttons

Nothing fancy going on here. Let's see the whats planned on the software side:

* display time ¯\\\_(ツ)_/¯
* internet radio (some nice [soma.fm](http://soma.fm))
* alarm (just start the radio)
* pre-alarm (start off with some ambient forst tunes)
* decreasing snooze time (15-10-5-1 mins)

The feature definition is pretty rough and will get more detailed when seeing how everything works together.

### interface
A couple of years ago i had to setup a wifi-printer with a minimum set of hardware buttons and a very long and cryptic wifi password. Still having nightmares from this experience i want a nice web app to manage the radio stations and whatever else needs to be configured. Still there should be a small set of hardware buttons to switch on/off the alarm & radio and stuff.

### optional
Of course when building a custom device, everything is custom and the list of possible features is almost endless. So here is my collection of maybe things:

* turn on some 433mhz power sockets (lights) during the alarm
* use voice commands (for snoozing and controlling more 433mhz sockets)
* get some weather infos (current & forecast)
* display artist info from radio station
* put lights into the alarm clock (maybe some fancy RGB leds) for some artificial sunrise


### housing
Of course we also need an appropriate housing for the Pi, the display, the wires and everything. I checked ebay and found a nice old alarm clock for 1eur. I would love to re-use/purpose all the buttons and nobs on the thing to maintain the overall look and feel of the old beauty. In the next steps i will disassemble and everything and see how this eventually works out - or write some code first ;)

### end
So, that's about it. Check out the [RaspWakeUp](https://github.com/jlorek/RaspWakeUp) repository for some software progress, heat up your soldering iron and bring your old alarm clock into the IoT century. Cheers!