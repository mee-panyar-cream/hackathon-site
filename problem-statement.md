---
---


# Central Question
 
How might we develop a remote monitoring capability that allows us to monitor energy usage at the point of generation and perform basic system analysis, at the cheapest possible cost, in low / intermittent bandwidth environments, and with assumed limited technical capability of technicians on the ground?
 
## Problem Statement
The sustainability of remote, off-grid energy technologies relies heavily on timely and informed maintenance. Remote monitoring of these systems can provide real time information on system downtime, inefficiencies, consumption, and theft. Additionally, remote monitoring can support the local technician/manager in fulfilling maintenance agreements and plans.

Existing solutions exhibit the following problems:
Too expensive and too high tech: plenty of fully smart tech solutions are emerging, but these involve integrating a significant amount of new technology into environments where it might not be appropriate, and the costs are often unrealistic
Designed for household level monitoring, for markets where households can / want to use mobile money and have exposure to apps/devices. In rural markets in countries like Myanmar, this is not currently a feasible approach. Higher level, simpler, lower cost solutions would be much more realistic.
Are designed on the assumption that good internet speeds are available and always on, which is not the case for our target communities. We need to send minimal amounts of data on low bandwidth, and be able to fall back to SMS when 2g is unavailable
Are designed for expert-level remote monitoring. While we will facilitate that, our focus is on enabling locally trained technicians to support Operations & Maintenance. We will therefore need to focus on User Experience: easy to understand information; alerts & triggers that explain what the situation or problem is; and step-by-step instructions for remedial action to be taken. Contacting the remote monitoring team is a backup, rather than the happy path, for the use cases being developed against



## Components of Solution
 
### The metering (at the generator)
#### PoC: 
Monitor the power output by plugging a standard device into a wall socket
Send power flow data every 10s for PoC, configurable
Inefficiency can be tracked by a power flow that is statistically significantly below average
Downtime / theft can be tracked by absence of power
#### MVP:
1.  Monitor power outputted by the system (smaller grids are around 10kW all the way to larger grids of 45kW, AC)
1. Ability to shut off the system remotely
1. For hybridized systems: monitoring on panel voltage and current
1. Fuel gauge (analytics on rate of fuel consumption can help with system optimization/efficiency)
1. Low oil,  high temperature,  and similar other metrics to prevent the system from being damaged
1. Needs to be easily integrated into existing systems



### Sending data (from the generator to the cloud)
#### PoC:
1. Ability to send simple data burst every 10s on a 2G / 3G connection
#### MVP:
1. Determine if connectivity is down, switch to SMS alerts if so
1. Local storage of data
1. Ability to batch data upload on request

### Data platform
#### PoC:
1. Receive and store data sent from remote monitoring device
1. Display data as a timeline, with a graph and data table
#### MVP:
1. Display all datasets including oil / temperature metrics
1. Basic trend data (averages / spikes etc)
1. Ability to set and deliver alerts and maintenance reminders by SMS to technicians / other staff

## Proof of Concept / MVP

### PoC aim:
1. Monitor power from small solar panel / converter / AC output / monitor setup
1. Send data to a cloud service
1. Basic visualization of data being tracked


### MVP aim:
1. Monitor power (and fuel potentially) from pilot village grid 
1. Send power + other metric data to a cloud service
1. SMS backups
1. SMS alerts / maintenance reminders
1. Visualization of data including trend analysis

## Preparation Needed for PoC

There are some prerequisites for the physical locations that will support Hackathons, currently set to be Shanghai and Singapore:

1. A common Gitbhub account or similar
1. A common developer cloud instance on AWS or similar
1. An Arduino / IoT kit
1. An Instructibles guide to setting up the hardware needed for power reading


