---
toc: true
layout: post
description: Software architecture diagram
categories: [diagram]
title: Software architecture diagram
---
# Software architecture diagram

![]({{ site.baseurl }}/images/achitecture.png "Software Architecture")

For mybrewery a microservice arcitecture is proposed. The requirements of the system require the system to perform different tasks that might benefit from independent choices of technologies used. In a microservice architecture the processing of sensor data can use a different tech stack than the web application for the community or the brewing application. Moreover, in a larger team, members with different skill sets can work on each service. This, on the other hand, can also turn out to be a downside of a microservice architecture. Using several different technologies results in an overhead and larger teams since more specialists are needed.

## Edge Devices (Sensors)

Edge devices like the temperature sensors in the brewing devices can benefit from a highly specialized architecture. Cloud services like Microsoft Azure provide specialized services that handle the processing of a continuous data flow in a highly efficient manner. In terms of cost, cloud services might be a little bit more expensive, but they are billed by usage. Assuming that mybrewery is targeted at hobby brewers, there is no constant need for such a service. It is only needed while  brewing which justifies higher costs per usage instead of constant but slightly lower costs.

For now the software requires a constant flow of data from the temperature sensors while brewing. The data should be processed and monitored to see if the temperature is in a predefined range. For later analysis the data must be stored in a database. Since only the series of temperatures is of interest, the service is built on a Key Value Store to ensure efficient storage and easy analysis. Since internet cannot be ensured 100% of the time, a fall back strategy like local preprocessing and a storage to keep the data from one brewing process as back up is needed. The connected brewing application device should ensure a back up storage.

## Brewing Application

The brewing application should be available as native application on any mobile device. The app should use proprietary hardware of the device to connect to any edge sensor and exchange data. Moreover, the when connected to the internet, the application connects to the applications server to manage the brewing recipes and transfer the data from the ongoing or previous brewing session. The recipe data is stored in a relational database on the server. The technologies used for the app can be web technologies. There are several ways to provide web apps as native apps. Since development resources are limited the focus of the brewing application should be iPads as portable device. 

## Web Application (Community)

The web application can be added in a later stage of the project. It is used to let the community (family and friends of the brewer) rate different brews. The results of the rating and comments should be stored in a relational database system and linked to the data from the brewing process. Whether or not the data is stored in the same database as the data from the brewing application needs to be evaluated. The brewing application has other requirements concerning availability and performance. Therefore, the seperation of both databases is proposed to ensure best performance for both systems. Whenever a new brew is finished in the brewing application, the information needed (name, style, ...) can be moved to the community database. Data consistency can be neglected and synchronisations times are not essential. As a prefered alternative an Application Programming Interface (API) is implemented. Moreover, the seperation is also in line with the microservice philosophy.

## Data Storage & Analytics

A lot on storage technologies has already been mentioned above. There will be a Key Value Store for sensor data and relational databases for both, the brewing application and the community website. While all databases might exchange some information via API, the data will remain within the service as single source of truth. For analytics purposes like for example the taste ratings and comments or temperture curves, the data form all databases will be integrated into the analytics service. Data from different services can be connected using the brewing session id.

For tracking brewing sessions the logging of different actions, especially the interactions with other parts of the software seems appropriate or even necessary. Whenever the edge device application returns values or the brewing session triggers a change in temperature, the respective information should be logged to a logfile. Moreover, any manual interference with the heater should be logged. Yet, logging should not be exaggerated and only be applied in critical processes and for tracking error states.