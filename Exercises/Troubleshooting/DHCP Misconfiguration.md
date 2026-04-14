## PROBLEM

-The system was unable to access the network due to incorrect IP configuration, preventing it from receiving proper settings from DHCP.

## ENVIRONMENT

-WINDOWS 10/11

## ROOT CAUSE

-IP address has been incorrectly configured which disallows it from accessing the Dynamic Host Configuration Protocol(DHCP)

## DIAGNOSIS

-Diagnose the issue by testing issue by opening command prompt

-Test ping 8.8.8.8 to test the internet

-Run ping google.com to test the Domain Name System(the system that translates domain names into IP addresses)

-Finally test ipconfig to see if the IP address being used is set correctly/incorrectly

## STEPS TAKEN TO RESOLVE ISSUE

-Open command prompt,then enter >ncpa.cpl->right-click ethernet

-Then enter properties->double click IPv4

-<img width="1148" height="716" alt="image" src="https://github.com/user-attachments/assets/06d50f61-10c4-43bd-9652-8660fa85afb8" />

-From the image the manual set IP address is incorrectly set as well as the DNS server

-Click the options that allow you to obtain IP address and and DNS server automatically

-re-enter the commands used in the diagnosis to re-test ip address and DNS

<img width="512" height="425" alt="image" src="https://github.com/user-attachments/assets/456e115f-6c2a-482c-900e-4255b0355966" />



-


