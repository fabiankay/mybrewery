---
toc: true
layout: post
description: Data Flow diagram
categories: [diagram]
title: Data Flow diagram
---
# Data Flow diagram

![]({{ site.baseurl }}/images/dataflow.png "Data Flow Diagram")

The Data Flow Diagram above shows the flow of information during a brewing session. It helped understanding the data access and exchange required during different stages of the process. In combination with the software's architecture, it gets clear where APIs or other access points for data exchange need to be established between different parts of the software. For example the recipe data is stored in another database than the sensor data.