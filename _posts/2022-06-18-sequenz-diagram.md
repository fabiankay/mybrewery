---
toc: true
layout: post
description: Sequenz diagram
categories: [diagram]
title: Sequenz diagram
---
# Sequenz diagram

![]({{ site.baseurl }}/images/sequenz.png "Sequence Diagram")

A sequence diagram shows the behaviour of and the interaction between differnt objects in a software. The diagram helps the user to understand the sequenze and results of actions during the process described. The sequenz diagram above shows the interaction of the brewing session with the user, the temperature sensor and the heater. The brewing session and the recipe define a target temperature. During the session, the temperature recorded from the sensor is compared to the target temperature. Depending on the outcome, the heater is turned on or off. All the information gathered is reported to the user and stored in the database. The whole sequence is ordered chronologically.

Drawing the sequence diagram really helped understanding the timely dependence of certain steps in the process. Generally, the learning from this and the diagrams before is that they can help communicating the idea in a standardized way and think about different implementation strategies without investing too much time into coding. Yet, keeping up all modelling rules and drawing a complete representation of the software is also very time consuming and for some parts feels like overhead. 