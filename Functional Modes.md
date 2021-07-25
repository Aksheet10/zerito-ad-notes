# Functional Modes

---

As well as Windows computers, domains/forest can also have their own "version", that is called [functional mode](https://docs.microsoft.com/en-us/troubleshoot/windows-server/identity/raise-active-directory-domain-forest-functional-levels). Depending on the mode of the domain/forest, new characteristics can be used.

The modes are named based on the **minimum Windows Server operative system required to work with them**

-   Windows2000
    
-   Windows2000MixedDomains
    
-   Windows2003
    
-   Windows2008
    
-   Windows2008R2
    
-   Windows2012
    
-   Windows2012R2
    
-   Windows2016

```powershell
PS C:\Users\Administrator\Downloads> (Get-ADForest).ForestMode
Windows2016Forest

PS C:\Users\Administrator\Downloads> (Get-ADDomain).DomainMode
Windows2016Domain
```


If you found a domain/forest with Windows2012 mode, you can know that all the Domain Controllers are at least Windows Server 2012.