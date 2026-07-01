## WHAT ARE GROUP POLICY OBJECTS?

- GPOs are simply a collection of settings that can be applied to OUs. 

## GROUP POLICY MANAGEMENT

-When you open the Group Policy Management console, the first thing you will see is the complete organizational unit (OU) hierarchy you created earlier. To configure Group Policy, you first create a Group Policy Object (GPO) under Group Policy Objects, and then link it to the OU where you want the policy settings to take effect. As an example, you can see that several GPOs already exist in your environment:

<img width="500" height="585" alt="Screenshot 2026-07-01 221542" src="https://github.com/user-attachments/assets/0d36f012-4ba3-4176-b0d0-a04a357e7a76" />

-> As shown above, three GPOs have already been created. The **Default Domain Policy** and **RDP Policy** are linked to the **thm.local** domain, meaning they apply across the entire domain. In contrast, the **Default Domain Controllers Policy** is linked only to the **Domain Controllers** OU and applies exclusively to domain controllers.

> One important concept to understand is that a GPO applies not only to the OU or domain to which it is linked, but also to all of its child OUs. For example, because the **Sales** OU is a child of the **thm.local** domain, it inherits the settings from the **Default Domain Policy**.

> To better understand the contents of a GPO, let's examine the **Default Domain Policy**. When you select a GPO, the first tab displayed is the **Scope** tab, which shows where the GPO is linked within Active Directory. In this case, the policy is linked only to the **thm.local** domain:

<img width="500" height="596" alt="Screenshot 2026-07-01 221721" src="https://github.com/user-attachments/assets/cc6c61b1-21d4-46c9-9600-39e4108536b6" />

-As shown above, you can also use Security Filtering to limit the application of a GPO to specific users or computers within the linked OU. By default, a new GPO applies to the Authenticated Users group, which includes all authenticated users and computers in the domain.

The Settings tab displays the actual contents of the GPO, allowing you to view the specific configurations it enforces. As mentioned earlier, a GPO can contain both Computer Configuration settings, which apply to computers, and User Configuration settings, which apply to users. In this example, the Default Domain Policy contains only Computer Configuration settings:

<img width="500" height="612" alt="Screenshot 2026-07-01 221914" src="https://github.com/user-attachments/assets/1975fcf1-a5bd-4bb4-8758-f87b095e64ff" />

> Because this GPO is linked to the entire domain, any changes made to it will affect all computers within the domain. As an example, let's modify the **Minimum password length** policy to require passwords to contain at least **10 characters**. To make this change, right-click the **Default Domain Policy** and select **Edit**:

<img width="442" height="393" alt="Screenshot 2026-07-01 222227" src="https://github.com/user-attachments/assets/c020286a-e2b3-4ebd-bacc-2e0c2cdaaff4" />

-> This opens the **Group Policy Management Editor**, where you can browse and modify all available policy settings. To change the minimum password length, navigate to **Computer Configuration** → **Policies** → **Windows Settings** → **Security Settings** → **Account Policies** → **Password Policy**, then open **Minimum password length** and set the required value to **10 characters**:

<img width="500" height="578" alt="Screenshot 2026-07-01 222441" src="https://github.com/user-attachments/assets/48d7216c-f818-45c1-ac3e-fa0fff4c5d41" />

-As you can see, plenty of policies can be established in a GPO. While explaining every single of them would be impossible in a single room, do feel free to explore a bit, as some of the policies are straightforward. If more information on any of the policies is needed, you can double-click them and read the Explain tab on each of them:

<img width="436" height="531" alt="Screenshot 2026-07-01 222619" src="https://github.com/user-attachments/assets/d25196da-2bc6-4b1a-bc60-b452fc74d89d" />








