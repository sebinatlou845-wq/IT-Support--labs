## SEPERATING PCs FROM SERVERS 

-By default, all the machines that join a domain (except for the DCs) will be put in the container called "Computers". If we check our DC, we will see that some devices are already there:

<img width="500" height="442" alt="Screenshot 2026-06-30 135016" src="https://github.com/user-attachments/assets/bf7b7b8a-397b-4a59-a92a-9c2e693ca5b2" />

-We can see some servers, some laptops and some PCs corresponding to the users in our network. Having all of our devices there is not the best idea since it's very likely that you want different policies for your servers and the machines that regular users use on a daily basis.

While there is no golden rule on how to organise your machines, an excellent starting point is segregating devices according to their use. In general, you'd expect to see devices divided into at least the three following categories:

## WORKSTATIONS

-These are the most common devices in an Active Directory domain. Most users will log on to a workstation to perform their daily tasks, such as accessing applications, creating documents, or browsing the web. Because workstations are more likely to be exposed to security threats, privileged accounts should never be used to sign in to them.

## SERVERS

-Servers are the second most common type of device in an Active Directory domain. Their primary role is to provide services to users and other systems, such as file sharing, web hosting, database services, authentication, and application hosting. Because servers often host critical services, they are typically managed separately from user workstations and are subject to stricter security and administrative policies.

## DOMAIN CONTROLLERS

-Domain controllers are among the most critical systems in an Active Directory environment. They are responsible for managing the Active Directory domain by authenticating users, enforcing security policies, and maintaining the directory database. Because domain controllers store sensitive information, including password hashes for all domain user accounts, they are considered some of the most secure and closely protected devices in the network.

To better organize our Active Directory environment, let's create two new organizational units (OUs): Workstations and Servers. There is no need to create a separate OU for domain controllers, as Windows automatically places them in the built-in Domain Controllers OU.

<img width="777" height="382" alt="Screenshot 2026-06-30 151218" src="https://github.com/user-attachments/assets/04631406-4dd5-4bbe-9561-2d8b7b23fb60" />

-> Next, move all desktop PCs and laptops from the **Computers** container to the **Workstations** OU, and move all servers to the **Servers** OU. Organizing devices into separate OUs allows you to apply different Group Policy settings and administrative controls to each category of devices as needed.
