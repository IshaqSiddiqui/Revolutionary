# Level 1 - Azure AD (Entra ID), HackMac, Series of Cloud Directory Escalation Challenges

## Contents 
* Background
* Logging in
* Scope of Access Level 1 and why
* Getting into level 2

### Background 

This is the first challenge in a series of unorthodox cloud directory escalation challenges. In this challenge you will learn to navigate the Azure portal and sift through what you do and do not have access to. If you solve all stops within this challenge, you will gain access to level 2 in this series. In order to solve level 1, you will need to solve several crypotgraphy challenges. 

## Logging into Azure Portal. 

* Using given username and password, navigate to portal.azure.com. For those not involved in Hackmac, please use the following credentials (these will be refreshed cyclically)
 | Password | 
 ---------  ----------
| level1test@hackedathackmac23.onmicrosoft.com | Ev3ryP@sswrodN33dsSecurit!1 | 


| Username  | Password |
| ------------- | ------------- |
| level1test@hackedathackmac23.onmicrosoft.com  | Ev3ryP@sswrodN33dsSecurit!1  |

* Try playing around, you will notice you do not have access to much. In fact, you will not even be able to access Entra ID. This is what you will be able to see if you try navigating.

### What Entra ID access attempt will look like 

<img width="1227" alt="image" src="https://github.com/IshaqSiddiqui/Revolutionary/assets/100017925/70c55262-5b8a-4b04-82a9-a88a25ddef0d">

#### Why can users in level1 not access Entra ID? - Admins have blocked access to administration portal. This is NOT a Security measure. 

<img width="1227" alt="image" src="https://github.com/IshaqSiddiqui/Revolutionary/assets/100017925/a5f97927-3d0b-4351-a2ff-9a1db0b52a31">

  * We can now block access to Entra ID portal using conditional access policies. At the time of creating the challenge this was not the case. It is advised you do not use this policy as a security measure. Rather refer to documentation [here][Correct Docs]

[Correct Docs]: https://learn.microsoft.com/en-au/entra/fundamentals/users-default-permissions#restrict-member-users-default-permissions

### Navigating around Azure Portal 

Where do you go next you would wonder. Where is the first challenge and how will you gain access to level 2? This is not black and white. Maybe you could find out what you have/don't have access to via [Graph][Grapha]? Maybe you would play around for a bit and notice that if you go to search resource groups in the search bar you will see this -> 

<img width="1227" alt="image" src="https://github.com/IshaqSiddiqui/Revolutionary/assets/100017925/ac592ec4-7aa4-4867-8aa0-0839a27b77d3">



* Might be worth understanding scope and management for Azure [here][Scope]

<img width="592" alt="image" src="https://github.com/IshaqSiddiqui/Revolutionary/assets/100017925/56705416-66f6-4596-91a0-e444844d65de">

### So you can see a resource group, now what? 
* What can you do within this resource group? What access do you have

<img width="1228" alt="image" src="https://github.com/IshaqSiddiqui/Revolutionary/assets/100017925/5b137cfd-4f18-4558-95ba-6c940e8e87b0">

### Notice that being a reader of the group doesnt mean you can read everything inside! You're also a privileged file reader.

<img width="1228" alt="image" src="https://github.com/IshaqSiddiqui/Revolutionary/assets/100017925/2d60dc7f-2790-4597-b264-81babc09effe">






[Grapha]: https://developer.microsoft.com/en-us/graph/graph-explorer
[Scope]: https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/overview





