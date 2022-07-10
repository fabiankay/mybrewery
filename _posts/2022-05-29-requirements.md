---
toc: true
layout: post
description: Requirements for the application.
categories: [requirements]
title: Requirements
---
# Requirements

## Functional Requirements
- [ ] The application must be able to plan the brewing process.
    - [ ] The user must be able to select the type of beer he/she wants to brew.
    - [ ] The user must be able to select the amount of grains he/she wants to use.
    - [ ] The user must be able to select the amount of water he/she wants to use.
    - [ ] The user must be able to select the amount of yeast he/she wants to use.
    - [ ] The user must be able to select the amount of hops he/she wants to use.
    - [ ] The user must be able to select the amount of time he/she wants to spend brewing.
    - [ ] The user must be able to specify each ingredient's quantity.
    - [ ] The user must be able to define the different steps of the brewing process and the time each step takes.
    - [ ] The user must be able to add a note to the brewing process.
    - [ ] The user must be able to save the brewing process.
    - [ ] The user must be able to load a previously saved brewing process.
    - [ ] The user should be able to see a list of all saved brewing processes.
    - [ ] The user should be able to delete a previously saved brewing process.
    - [ ] The user should be able to specify the name of the beer.
    - [ ] The user should be able to specify the type of malt used.
    - [ ] The user should be able to specify the type of hops used.
- [ ] The application must be able to monitor the brewing process.
    - [ ] The user must be able to see the current step of the brewing process.
    - [ ] The user must be able to see the remaining time for the current step of the brewing process.
    - [ ] The user must be able to see the current temperature of the brewing process.
    - [ ] The user should be able to see the amount of ingredients needed for the current step.
    - [ ] The user should be able to see the next step of the brewing process.
    - [ ] The user should be able to see the amount of ingredients needed for the next step.
- [ ] The application must be able to document the brewing process.
    - [ ] The application must store all the information collected during the brewing process.
    - [ ] The collected data must be available for every brewing process.
    - [ ] The user must be able to add comments for each step.
    - [ ] The user should be able to comment or add tasting notes.
    - [ ] The user should be able to rate the beer after the brewing.

## Technological Requirements
- [ ] The collected data must be stored accessible and persistent.
- [ ] Edge sensors (f.e. temperature sensors) must be integrated so they can be exchanged or extended easily.
- [ ] Users must authenticate before using the application.
- [ ] The application must work without internet connection.
- [ ] The application should provide users the option to share their brewing processes publicly or privately.

## Quality of Service
- [ ] The application must be available through all common internet browsers in their latest version.
- [ ] The application should be available on tablet devices.

## User Interface Requirements
- [ ] The temperature data should be available as line chart.
- [ ] The user must be able to access and see the data collected during the brewing process in a human readable way.
- [ ] The application should be responsive and optimized for tablet usage.
- [ ] The application could have a dark mode (because everything cool should have a dark mode ;) ).

## Legal and contractual Requirements
- [ ] The application must support measurement units for the following:
    - [ ] Liquid volume in liters
    - [ ] Weight in kilograms
    - [ ] Temperature in degrees Celsius
    - [ ] Time in minutes
    - [ ] Gravity in SG
- [ ] The application must be available in english.
- [ ] The application should be available in german.

## Changes of requirements
Requirements can change rapidly. Therefore, having a plan how to deal with changes is essential for ongoing success.
To effectively deal with changing requirements, it helps to classify and document changes regardless of their "size".
For this project I propose categorizing any changing requirements by the following factors:
- severity (high, medium, low)
- source (internal, external)
- effect (effected part of the software)
- reason/description (for documentation)
- result/decision (add, adapt, remove)

Depending on the classification of changing requirement, different processes should be applied.
For severe external as well as external changes the project team should decide how to incorporate the change immediately.
For less severe changes the team should decide after the current iteration.
For non severe changes individuals or the team in charge of the effected part of the application may decide.

Potential changes might come from covering other "markets" in terms of localization. F.e. for US usage, the units and calculations need to be adapted. Moreover, some speciality beer styles might require special types of ingredients (flavoring) or additional steps (dry-hopping).