## KERBEROS

- Used by any recent version of Windows. This is the default protocol in any recent domain.

## NetNTLM

- Legacy authentication protocol kept for compatibility purposes.

## KERBOS AUTHENTICATION

-> **Kerberos** is the default authentication protocol used by modern versions of Windows. When a user authenticates to the domain using Kerberos, they are issued **tickets** that serve as proof of successful authentication. Instead of repeatedly entering credentials, users present these tickets to access services, allowing the services to verify that the user has already been authenticated by the domain and is authorized to use the requested resource.

-When Kerberos is used for authentication, the following process happens:

 > During the initial authentication process, the user sends their username along with a timestamp encrypted using a key derived from their password to the **Key Distribution Center (KDC)**. The KDC, which typically runs on a domain controller, is responsible for issuing Kerberos tickets.

> After validating the user's credentials, the KDC issues a **Ticket Granting Ticket (TGT)**. The TGT allows the user to request additional tickets for specific services without having to resend their credentials each time they access a network resource. Along with the TGT, the KDC also provides a **session key**, which the client uses to authenticate subsequent requests.

> Although requiring a ticket to obtain more tickets may seem unusual, this design improves both security and efficiency by preventing repeated transmission of user credentials across the network.

> The TGT itself is encrypted using the password hash of the **krbtgt** account, which means the client cannot read or modify its contents. The encrypted TGT also contains a copy of the session key. Because the KDC can decrypt the TGT using the **krbtgt** account's secret, it can recover 
the session key whenever needed without storing it separately.

## NetNTLM AUTHENTICATION

-NetNTLM works using a challenge-response mechanism. The entire process is as follows:

> The NTLM authentication process works as follows:

1. The client sends an authentication request to the server it wants to access.
2. The server generates a random value, known as a **challenge**, and sends it to the client.
3. The client uses its **NTLM password hash**, together with the challenge and other protocol data, to calculate a **challenge response**, which is then sent back to the server.
4. The server forwards both the challenge and the client's response to the **Domain Controller** for verification.
5. The Domain Controller performs the same calculation using the user's stored NTLM password hash and the original challenge. It compares the computed response with the one received from the client. If they match, the user is successfully authenticated; otherwise, authentication fails.
6. The Domain Controller returns the authentication result to the server, which then informs the client whether access has been granted or denied.


