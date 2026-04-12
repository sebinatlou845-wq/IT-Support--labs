## PROBLEM 

-WIFI is connected but websites are not opening indicating a DNS resolution failure

## ENVIRONMENT

-WINDOWS 10

## ROOT CAUSE

-Incorrect DNS server configuration prevented domain names from being resolved into IP addresses

## STEPS TAKEN TO SOLVE ISSUE

-Diagnose the issue with ping 8.8.8.8 and ping google.com

<img width="700" height="739" alt="Screenshot 2026-04-12 091015" src="https://github.com/user-attachments/assets/b916aef3-800b-454d-bdf3-e10b5c387ae5" />

ping 8.8.8.8 responds with 'reply from',which therefore means that internet has responded positively,ping google.com could not find a host which therefor means that a DNS failure has occured

-enter settings ,then enter network and internet >change adapter options>right-click ethernet>enter proprties>enter IPv4

<img width="700" height="719" alt="Screenshot 2026-04-11 000535" src="https://github.com/user-attachments/assets/ee670ebd-6d5e-4b4f-8db6-8f5ee1501e07" />

-you can either manually enter a functional DNS server or obtain IP address automatically

<img width="700" height="716" alt="image" src="https://github.com/user-attachments/assets/cc1c3199-835b-4d72-b56c-5b5f75398a62" />

-After applying 'obtain IP address automatically" we redo ping 8.8.8.8 and ping google.com

<img width="700" height="716" alt="image" src="https://github.com/user-attachments/assets/3742ccc4-fe4c-4f6e-8345-92dd807a1eec" />

-Now everything has responded positively

## CONCLUSION

-Both the internet and DNS have responded positively,therefore DNS has successfully been configured








