# Agenda :mushroom:

### 1. Aims :bar_chart:
### 2. Structure :evergreen_tree:
### 3. Accidents and Fumbles :ghost:
### 4. Solves :unlock:

## Aims 

* Educate participants about navigating through Azure Active Directory(Entra ID). Discovering misconfigurations, how conditional access policies work, how PIM works and circumventing conditions to escalate through the Entra ID.

## Structure 

# Users within groups who have access to resource group
  
![image](https://github.com/IshaqSiddiqui/Revolutionary/assets/100017925/8458d12b-0f82-4388-91c6-ece5150bdc8b)

* Above we can see a number of resource groups. They may or may not have roles assigned to them. Being a global admin in Entra ID for example, does not by default ensure that user is assigned an Role in this Resource Group. 

# Each resource *group* has access controls
  
![image](https://github.com/IshaqSiddiqui/Revolutionary/assets/100017925/e44cb7f3-7ad1-4a39-a25f-aefade55a303)

* Alluding to point made above. We can see access controls on the left hand side of this resource group. 

# Each resource within a group has access controls
![image](https://github.com/IshaqSiddiqui/Revolutionary/assets/100017925/4f441177-c5dc-4b23-bdaa-8725ff15af83)

[Read more on what Access Control is][recent]

[recent]:https://www.microsoft.com/en-au/security/business/security-101/what-is-access-control

## Example of creating blob storage (a resource) 

![image](https://github.com/IshaqSiddiqui/Revolutionary/assets/100017925/0f7c2e21-68e4-4625-944e-6486ab2bc310)

## Settings of blob storage 
* authentication only through Azure
* LRS, locally redunundant storage, lowest cost available

## How are groups organised? 
1. Dynamic Groups (cannot have roles with Azure, Entra)
2. Assigned Groups (can have roles assigned within Azure, Entra)

  
## Dynamic Groups 

#### A dynamic group is a group that dynamically adds or removes users based on properties.

#### Note: A dynamic group can be used to automatically add or remove users based on user properties. User Attributes is not synonymous with user properties. 

### Example of a dynamic Group


#### Example of condition of entry 
![image](https://github.com/IshaqSiddiqui/Revolutionary/assets/100017925/5c9cb3ed-ec6d-4e15-b25b-dc3a5ee46b75)



### Tangent on Security Atributes 

### What about custom security attributes
![image](https://github.com/IshaqSiddiqui/Revolutionary/assets/100017925/50cc2821-0c12-4fa8-b2ef-a388300292d8)

#### Custom Security attributes can be used to give access to blob storage, 

See [here][customattr] - 

> Custom security attributes in Microsoft Entra ID are business-specific attributes (key-value pairs) that  you can define and assign to Microsoft Entra objects. These attributes can be used to store information,  categorize objects, or enforce fine-grained access control over specific Azure resources. Custom security attributes can be used with Azure attribute-based access control (Azure ABAC).

[customattr]: https://learn.microsoft.com/en-us/azure/active-directory/fundamentals/custom-security-attributes-overview







## Accidents and fumbles 
* Accidentally made administrative units with restricted access, preview feature. Now there are licensed redunant users that not even the global admin can edit.

## Solves 
* In each section




