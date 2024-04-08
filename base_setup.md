Once your root server provisioning is complete you will get an email with it's public IP address and the password to login as root.

Root servers come preinstalled with a "rescue system" which allows the installation of the full server with a single command.

From a terminal logging into your root server using:
```ps
ssh root@ip_of_your_server
```
You will get the prompt:
```bash
root@rescue ~ #
```
From this prompt run:
```sh
installimage
```
On the install menu select:
- Debian
- Debian-1205...
- \<OK\> to the notice
- On the editor do not do any change, just press F10

The installation will take =~ 3mins

Once the installation completes, type:
```sh
reboot
```
After 1 min check that your server is available:
```sh
ssh root@ip_of_your_server
```


    WARNING: As you previously logged in to the same IP you will get an "Host key verification failed" error, you will need to delete the line with the IP from the file .ssh/known_hosts:6

After logging into the server you now should get the Debian prompt:
```sh
root@Debian-1205-bookworm-amd64-base
```