
# nHC/CSH pROJECT

## Introduction

The nHC project stands for nano-House-Controller project.  The idea of the nHC is a network of ioT devices around the house that ensures a connected smart house(CSH).

The main features of this project include:

1. Low power controllers that can be powered over months
2. Collection of trivial parameters including motion sensing, temperature, humidity, ambiency etc.
3. Miniature control of trivial parameters plus an digital/analog i/o controller/actuation extension.
4. interconnectivity of the controllers to a central hub that will have internet connectivity.
5. wireless connectivity of devices

The system diagram for the nHC project is as follows:
![Figure 1](https://selene.hud.ac.uk/u1273400/images/seg_media/nhc.PNG)
**Figure 1:** System diagram for the nHC project

## Design

The setup of the nHC project consists two major players.  The hub and the nano-controllers (ncs or minions). The overall goal of the minions is the most compact design having low power extended battery life.  In theory, the smaller the components are the less power they are to consume therefore, thankfully, both goals compliment each other and do not counteract each other.  On the other hand however, each of the constraints of power and minitaurisation requires a significant amount of engineering to achieve a production-satisfactory level of implementation.  The hub is the data aggregator, controller and communications hub.  Essentially the hub is the nHc system's link to the outside world offering both communications and control of the nHC system from the outside world.

### Minion Components
The minion will comprise the following components

1. Microcontroller chip
2. radio chip
3. buzzer
4. temperature humiditycontroller
5. motion sensor
6. io extesion

The block diagram for the minion is as follows:
![Figure 2](https://selene.hud.ac.uk/u1273400/images/seg_media/minion_bd.PNG)
**Figure 2:** Block diagram for minion nano-controller

#### The Microcontroller

The STM32L0 is the micrcocontroller of choice for the nHC project. This microcontroller, in addition to standard interfacing features to the outside world also offers low power features that are desirable for the nHC specification.

#### The radio chip
<img src="https://selene.hud.ac.uk/u1273400/images/seg_media/e82.jpg" width="200">
**Figure 2:** 433MHz wireless radio module
<img src="https://selene.hud.ac.uk/u1273400/images/seg_media/e72.jpg" width="200">
**Figure 3:** 2.5GHz wireless radio module

#### The Buzzer

#### The Temperature/humidity chip
<img src="https://selene.hud.ac.uk/u1273400/images/seg_media/e42.jpg" width="200">
**Figure 5:** 433MHz wireless radio module

#### The PR motion sensor
<img src="https://selene.hud.ac.uk/u1273400/images/seg_media/e32.jpg" width="200">
**Figure 6:** PR motion sensor

#### io extention

### The nHC Hub
The nHC hub will comprise the following components

1. Microcontroller chip
2. radio chip
3. gprs module
4. wireless controller
5. microstorage (sdcard)

The block diagram for the hub is as follows:
![Figure 1](https://selene.hud.ac.uk/u1273400/images/seg_media/hub_bd1.PNG)
**Figure 7:** Block diagram for the hub sub-system

#### The Microcontroller chip

The STM32L0 is the micrcocontroller of choice for the nHC project. This microcontroller, in addition to standard interfacing features to the outside world also offers low power features that are desirable for the nHC specification.

#### The radio chip

#### The sd-card

#### The wireless controller
<img src="https://selene.hud.ac.uk/u1273400/images/seg_media/e52.jpg" width="200">
**Figure 8:** Wifi module
<img src="https://selene.hud.ac.uk/u1273400/images/seg_media/e62.jpg" width="200">
**Figure 9:** Wifi module

#### GPRS module
<img src="https://selene.hud.ac.uk/u1273400/images/seg_media/e12.jpg" width="200">


## Bill of Quantities
The summary of the items required for a single unit of the nHC project are as follows

1. Microcontrollers x2
2. radio chip x 2
3. sd-card
4. gprs module
5. wifi module
6. pr motion sensor
7. temp/humidity sensor
8. buzzer

### Cost of Equipment

| S/N| Item                                            | Description                  | Price   |
|----|-------------------------------------------------|------------------------------|---------|
| 1  | [STM32L0](http://goo.gl/NYH8es)                 | Microcontroller              |   £3.03 |
| 2  | [RF SOLUTIONS,ZETA-433](http://goo.gl/tCDqYV)   | 433 Mhz Radio module         |   £5.67 |
| 3  | [MICROCHIP,MRF89XAM9A-I/RM](http://goo.gl/KUlhgn)| Sub-GHz radio module        |   £5.67 |
| 4  | [MICROCHIP,MRF24J40MA-I/RM ](http://goo.gl/UI2hqJ)| 2.5Ghz radio module        |   £5.64 |
| 5  | [Buzzer](http://goo.gl/kK7Ob1)                  | Buzzer                       | £1.59   |
| 6  | [IST INNOVATIVE SENSOR TECHNOLOGY,HYT 271,SENSOR](http://goo.gl/PIkQWk) | Temperature/ humidity sensor |  £26.49 |
| 7  | [MURATA,IRA-E700ST0](http://goo.gl/kvGDDD)      | PIR motion sensor            | £2.38   |
| 8  | [SEGGER,6.20.13 SD CARD ADAPTER](http://goo.gl/k7MZLh)| SDCARD adapter               | £103.97 |
| 9  | [TELIT WIRELESS SOLUTIONS,GE863GPS730,MODULE](http://goo.gl/rWhBLW)| GPRS module | £60.29  |
| 10 | [MICROCHIP,MRF24WB0MA/RM](http://goo.gl/DsCdIA) | Wifi Module                  | £12.99  |
