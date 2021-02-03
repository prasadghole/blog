---
title: "CAN Summary"
date: 2021-02-03T11:34:54+05:30
lastmod: 2021-02-03T11:34:54+05:30
draft: false
keywords: []
description: "CAN protocol summary"
tags: ["development"]
categories: []
author: ""

# You can also close(false) or open(true) something for this content.
# P.S. comment can only be closed
comment: false
toc: tru
autoCollapseToc: false
postMetaInFooter: false
hiddenFromHomePage: false
# You can also define another contentCopyright. e.g. contentCopyright: "This is another copyright."
contentCopyright: false
reward: false
mathjax: false
mathjaxEnableSingleDollar: false
mathjaxEnableAutoNumber: false

# You unlisted posts you might want not want the header or footer to show
hideHeaderAndFooter: false

# You can enable or disable out-of-date content warning for individual post.
# Comment this out to use the global config.
#enableOutdatedInfoWarning: false

flowchartDiagrams:
  enable: false
  options: ""

sequenceDiagrams: 
  enable: false
  options: ""

---

<!--more-->
# Controller Area Network (ISO 11989-1) 
It is a multidroo serial bus providing physical and data link layer specifications
for connecting mutiple participant nodes.
On physical layer it uses diffrenrtial electical signal.


# Key features
- Excellent noise immunity
- Multi master 
- Priority based messageing
- Error checking
- Industrial standard with many suppliers
- Data rate from 5Kb/s to 1Mb/s
- Cable length from 40m (1Mb/s) to 1000m (40Kb/s)
- Multidrop with maximum 127 nodes
- Asynchronus transmission

# Singal logic levels
It uses Non return to zero NRX coding.
- Recessive 
Logic 1
- Dominant 
Logic 0

## Bit stuffing
Due to NRZ method a proper continours signal of transmitting same bit may cuase
recever to think its in error stage. Hence bit stuffing method is used.

Sender send complement value if it detects five bits with same value to be transmitted
Receiver will also discard the stuff bit value.t/CANFrame.jpg)

## Data frame
## Remote frame
## Overload frame
## Error frame
  
# Communication Protocol
Access to bus is by using carrier sense multiple access with collision detection
called bitwise arbitration. Bus normally remain in recessive state. To transmit
node first checks for inactivity and sends a frame to bus. For simulatanious 
transmission node with lower arbitration value take the bus.
Other nodes stops till other high priority nodes complete the transmission.


As CAN only provide details about physical and data link layer remaianing top
layers was not standardize in earlier versions. This caused complatibilities 
issues with diffrent vendores.

Various top level 3 to 7 standars are
## CANopen
Used for industrial machien control, medical, railways.

## DeviceNet
Used as fieldbus for factory automation. Maximum 64 nodes can be used till maximum
500 Kb/s.

## J1939
This is used in heavy trucks and buses. It uses 29 bit identifier.
