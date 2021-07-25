# Domains
---

### #Domain

An Active Directory network is what is usually known as a **Domain**.

A domain is a set of connected computers that shares an Active Directory database, which is managed by the central servers of a domain, that are called **Domain Controllers. Each domain have its own Domain Controllers**

---

### #Domain_Name

Each domain has a DNS name. In many companies, the name of the domain is the same as their web site, for example `contoso.com`, while others have a different internal domain such as `contoso.local`.

```powershell
PS C:\Users\Anakin> $env:USERDNSDOMAIN
CONTOSO.LOCAL
PS C:\Users\Anakin> (Get-ADDomain).DNSRoot
contoso.local
```
Identify current user domain from Powershell

> `$env:USERDNSDOMAIN`
`(Get-ADDomain).DNSRoot`
`(GetDomain).Forest`

```powershell
PS C:\Users\Anakin> (Get-WmiObject Win32_ComputerSystem).Domain
contoso.local
```
Identify current computer domain from Powershell

>(Get-WmiObject Win32_ComputerSystem).Domain

---

### #NetBIOS

 Every domain can also being identified with **NetBIOS** name. You can see the **NetBIOS** name being used in log in operations, where the user is identified with something like `CONTOSO\Administrator`, where the first part is the NetBIOS name and the second one is the username.
 
 ---
 ### #SID
 A domain can be identified by an **SID** (Security Identifier).
 
 The **SID** is **more used by programs** (using the Windows API) than users.
 
 ```powershell
PS C:\Users\Anakin> Get-ADDomain | select DNSRoot,NetBIOSName,DomainSID

DNSRoot       NetBIOSName DomainSID
-------       ----------- ---------
contoso.local CONTOSO     S-1-5-21-1372086773-2238746523-2939299801
```
We can obtain it via many commands.
 >`Get-ADDomain | select DNSRoot,NetBIOSName,DomainSID`