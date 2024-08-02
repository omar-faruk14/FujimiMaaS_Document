# ふじみ MaaS
Fujimi MaaS is a comprehensive platform designed to　streamline event organization and enhance user experience through real-time tracking and notifications. This project leverages a combination of modern technologies including LINE message, Reactjs, express, open route service api,  integration, AWS Lambda, Kintone, and AWS Amplify to deliver a robust serverless solution.



## Table of Contents

- [Introduction](#introduction)
- [Features](#Features)


## Introduction

The application interface for Fujimi MaaS includes an interactive map feature integrated with OpenStreetMap. The map displays various location markers, each representing different event venues or points of interest. By clicking on the "LINE Official Account" menu link, users can access this map view.

![Project Image](/img/map1.jpg)

Each marker on the map is linked to detailed event information specific to that location. Users can select a marker to view comprehensive details about the events happening at that place, enhancing their ability to find and participate in relevant activities.

## Facilities_Section

The facilities details page in Fujimi MaaS provides in-depth information about the amenities available at each event location. This page displays a comprehensive list of facilities associated with each venue, ensuring users are well-informed about the available services and features.

![Project Image](/img/facilities1.jpg)

For each location, the page outlines the various facilities provided, such as seating arrangements, accessibility options, and any additional amenities. This detailed overview helps users understand what to expect at each venue and plan their visit accordingly.

## Event Access Based on User Registration
In the Fujimi MaaS project, when a user clicks on "Jomon" or "Event List," the system first checks the user's registration status by querying the database. This is achieved using AWS Lambda and Kintone integration through a webhook.
![Project Image](/img/event_menu.png)

If Registered: The system retrieves the appropriate event links from the database and displays them to the user, allowing access to event details and further actions.
If Not Registered: The system notifies the user that they need to complete their registration to access the event information.
![Project Image](/img/jomon_menu.png)
This process ensures that only registered users can view event links and participate, streamlining the user experience and maintaining event security.



**Brief description**  of your project and what it aims to achieve.

## Features
- <span style="color: green; font-size: 18px;">Feature 1</span>


