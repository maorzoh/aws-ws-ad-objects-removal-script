# AWS WorkSpaces AD Computer Objects Removal Script
Removes AD computer objects (WorkSpaces) that are no longer exist in AWS WorkSpaces.


### Overview

This PowerShell script helps keep Active Directory synchronized with AWS WorkSpaces by identifying and removing AD computer objects that no longer correspond to existing WorkSpaces in AWS.

The script retrieves the current WorkSpaces and their computer names from AWS, compares them against the computer objects in a specified Active Directory OU, and automatically removes any AD computer objects that are no longer present in AWS WorkSpaces.

The script can be scheduled using **Windows Task Scheduler** on a Domain Controller or on a server with the **RSAT Active Directory PowerShell module** installed. It is recommended to run the script periodically, based on the organization's requirements.

The script also maintains a log file containing the cleanup activity, including successfully deleted objects and any deletion errors.
