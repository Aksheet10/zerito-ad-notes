# Forests

---

Using a DNS name is very useful, since it allows to specific subdomains being created for management purposes.

A company can have a **#root_domain** called `contoso.local`, and then subdomains for different (usually big) departments, like `it.contoso.local` or `sales.contoso.local`.
```
                  contoso.local -------------------> Forest
                        |
               .--------'---------.
               |                  |
               |                  |
Tree ---> hr.contoso.local  it.contoso.local ------> Forest
                		          | 
                 				  |
             	    			  |
  				        webs.it.contoso.local -----> Tree
 ```
 
 ````powershell
 Get-ADForest
````
This command can be used to get the information about the forest.

Each domain has its own database and its own Domain Controllers. **Users of a domain in the forest can also access to the other domains** of the forest.