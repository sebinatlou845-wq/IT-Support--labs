## PROBLEM

-User cannot access the internet even when connected

## ENVIRONMENT

-WINDOWS 10/11

## DIAGNOSIS

-Website has failed to load, therefore there is no internet

<img width="700" height="714" alt="image" src="https://github.com/user-attachments/assets/9fc78d92-67e0-4046-9975-e68f86680ce8" />

-IPconfiguration shows a working IP address,but command 'ping 8.8.8.8'has failed which indicates no internet connectivity

<img width="700" height="700" alt="image" src="https://github.com/user-attachments/assets/6981e5f4-1df7-48a4-8b99-a694a3bcfd85" />

-With a correct IP address, connected network and no internet connectivity ,this activity indicates that there is an issue that is blocking traffic(incorrect Windows Defender Firewall settings)

## STEPS TAKEN TO SOLVE ISSUE

-Enter Windows Defender Firewall ->Advanced settings->Outbound rules,in order to disable settings that are working aginst network connectivity

<img width="700" height="714" alt="image" src="https://github.com/user-attachments/assets/49903cb1-cf33-4bcd-96f9-7ca8b1bacdf2" />

-Once complete enter command prompt then enter 'ping 8.8.8.8' again to verify changed settings

<img width="700" height="717" alt="image" src="https://github.com/user-attachments/assets/94162770-0224-4540-a933-e6e8d6cc51e6" />

-Now with a positive reply from the command internet connectivity has now been restored

## CONCLUSION

-The device had a valid IP but couldnt reach external networks.I identified a firewall rule blocking outbound traffic and removed,restoring connectivity






