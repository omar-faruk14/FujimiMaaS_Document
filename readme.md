# ふじみ MaaS
Fujimi MaaS is a comprehensive platform designed to　streamline event organization and enhance user experience through real-time tracking and notifications. This project leverages a combination of modern technologies including LINE message, Reactjs, express, open route service api integration, AWS Lambda, Kintone, and AWS Amplify to deliver a robust serverless solution.

![Project Image](/img/Server-Less.jpg)

# Table of Contents

1. [Introduction](#introduction)
2. [Real-Time Vehicle Tracking](#real-time-vehicle-tracking)
3. [Facilities Section](#facilities-section)
4. [Event Access Based on User Registration](#event-access-based-on-user-registration)
5. [Event Section](#event-section)
    - [Features](#features)
    - [Event Management](#event-management)
6. [User Registration Integration](#user-registration-integration)
7. [Optimal Route](#optimal-route)
    - [Brute Force TSP Algorithm](#brute-force-tsp-algorithm)


## Introduction

The application interface for Fujimi MaaS includes an interactive map feature integrated with OpenStreetMap. The map displays various location markers, each representing different event venues or points of interest. By clicking on the "LINE Official Account" menu link, users can access this map view.

![Project Image](/img/map1.jpg)

Each marker on the map is linked to detailed event information specific to that location. Users can select a marker to view comprehensive details about the events happening at that place, enhancing their ability to find and participate in relevant activities.

## Real time vehicle Tracking
The Fujimi MaaS project includes a real-time vehicle tracking feature designed to enhance event management and user experience. This feature tracks vehicles involved in event operations, providing up-to-date information about their locations and status.

![Project Image](/img/realtime_tracking.jpg)

### Key Features
**Real-Time Vehicle Tracking:**
- Vehicles are tracked in real-time to monitor their locations and movements.
- The system identifies which vehicle is assigned to pick up or drop off event participants.

**Location Updates:**

- Vehicle locations are updated every minute in the database, while the application provides real-time updates.
- After each update, the vehicle's real-time location is recorded and stored in the database. This ensures that the data is up-to-date and accessible for real-time tracking and reporting.


## Facilities Section

The facilities details page in Fujimi MaaS provides in-depth information about the amenities available at each event location. This page displays a comprehensive list of facilities associated with each venue, ensuring users are well-informed about the available services and features.

![Project Image](/img/facilities1.jpg)

For each location, the page outlines the various facilities provided, such as seating arrangements, accessibility options, and any additional amenities. This detailed overview helps users understand what to expect at each venue and plan their visit accordingly.

## Event Access Based on User Registration
In the Fujimi MaaS project, when a user clicks on "Jomon" or "Event List," the system first checks the user's registration status by querying the database. This is achieved using AWS Lambda and Kintone integration through a webhook.

![Project Image](/img/event_menu.png)

If Registered: The system retrieves the appropriate event links from the database and displays them to the user, allowing access to event details and further actions.
If Not Registered: The system notifies the user that they need to complete their registration to access the event information.
<br>

![Project Image](/img/jomon_menu.png)

This process ensures that only registered users can view event links and participate, streamlining the user experience and maintaining event security.

## Event Section

The Event List Page allows users to view the latest events, with the nearest events appearing first. This page is fully dynamic, meaning all event data can be managed from the database.

![Project Image](/img/event_list.jpg)

### Features
**Latest Events Display:** The page shows the most recent events, sorted so that the nearest event appears first.

**Dynamic Data:** All event information is pulled from the database, allowing for real-time updates.
### Event Management:
**Publish/Unpublish:** Event organizers can publish or unpublish events directly from the database.
**Event Details:** Organizers can set various details for each event, including:
- Event Name
- Event Description
- Start Date
- End Date
- Application Start Date
- Application End Date

Register a user through a form or application that integrates with the LINE Official Account's LIFF system, allowing the page to load within the LINE app.

![Project Image](/img/line_message.jpg)

Upon successful completion, it will return a text message using LINE.

## Optimal Route

The Fujimi MaaS project aims to facilitate efficient event organization and provide transportation services in the Fujimi area. The primary goal is to optimize route planning to maximize the number of people picked up in the shortest possible time.
Real-time route planning ensures efficient pick-up and drop-off services, minimizing wait times.

**Route Optimization**

The system uses the OpenStreetMap API to retrieve distance and duration matrices between specified locations. A brute-force approach solves the Travelling Salesman Problem (TSP) to find the optimal route.

**Process:**

- Data Collection: Retrieve distance and duration matrices for all locations (start point, waypoints, and end point).
- Route Calculation: Determine the most efficient route using the distance matrix.
- Output: Provide a detailed route plan, including distances and durations between stops.
<br><br>

![Project Image](/img/optimal2.jpg)

### Brute Force TSP Algorithm

The Brute Force TSP (Traveling Salesman Problem) algorithm comprehensively evaluates all possible permutations of routes to find the optimal path that minimizes total distance or time. This algorithm guarantees finding the shortest path.

Implementation Details

Input: The algorithm takes a set of locations with their respective coordinates as input.
Process:

#### Generate all permutations of waypoints.
- Calculate the total distance for each permutation using a distance matrix.
- Select the permutation with the smallest total distance as the optimal route.
<br>

![Project Image](/img/optimal1.jpg)

<br>
**Output:** 
- The optimal order of locations and the corresponding distance and required time.



**Advantages:**

- Accuracy: By evaluating all possible routes, it guarantees the optimal solution.
- Simplicity: The algorithm is easy to implement and understand.






