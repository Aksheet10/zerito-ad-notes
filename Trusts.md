# Trusts

---

The users can access to another domains in the same forests because they are linked by connections called **#Trusts**.

The **[trust direction](https://docs.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2008-r2-and-2008/cc731404(v=ws.10)) is the opposite to the access direction**

```
 (trusting)         trusts        (trusted)
  Domain A  -------------------->  Domain B
       outgoing               incoming
       outbound               inbound
                    access
            <--------------------
```

Domain A trusts Domain B so Domain B can access Domain A.

Imagine it like you trust your friend. So he comes to your place and you let him access your resources.
That means he can access your resources.

When a trust is directed through your current domain in called an Inbound or Incoming trust. **Incoming trusts allow users of your domain to access the other domain**.

On the other hand there are Outbound or Outgoing trusts, that go from your domain to the other. Therefore the **users of the other domain can access to your domain**

