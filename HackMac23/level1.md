## Logging into Azure Portal. 

* Using given username and password, navigate to portal.azure.com
* Try playing around, you will notice you do not have access to much. In fact, you will not even be able to access Entra ID. This is what you will be able to see if you try navigating.

### What Entra ID access attempt will look like 

<img width="1227" alt="image" src="https://github.com/IshaqSiddiqui/Revolutionary/assets/100017925/70c55262-5b8a-4b04-82a9-a88a25ddef0d">

#### Why can users in level1 not access Entra ID? - Admins have blocked access to administration portal. This is NOT a Security measure. 

<img width="1227" alt="image" src="https://github.com/IshaqSiddiqui/Revolutionary/assets/100017925/a5f97927-3d0b-4351-a2ff-9a1db0b52a31">

  * We can now block access to Entra ID portal using conditional access policies. At the time of creating the challenge this was not the case. It is advised you do not use this policy as a security measure. Rather refer to documentation [here][Correct Docs]

[Correct Docs]: https://learn.microsoft.com/en-au/entra/fundamentals/users-default-permissions#restrict-member-users-default-permissions




