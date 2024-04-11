
Goto https://porkbun.com/account/domainsSpeedy

Click on the `DNS` link below the domain you want to use for your server.
On the record configuration form:
- In the `Current Records` press the trash icon to delete the CNAME *.hobbysite.dev
- On the `Host` field type "*" to have all names under this domain provided from this server
- On the `Answer` field provide the IP of the server.
- Click Add
- Click "X" To close the Window
The propatation of the new DNS configuration can take a few minutes.
To validate that the configuration was performed, run:
```
ping www.<your_domain>
```
The reply should come with the IP of the server.