
```sh
apt update
apt install caddy
```

Create the site config
```sh
mkdir -p /etc/caddy/sites-enabled/
cat > /etc/caddy/sites-enabled/www.hobbysite.dev << _EOF_
www.hobbysite.dev {

  # Your website specific configurations can go here
  root * /var/www/html
  file_server
}
_EOF_
echo hello > /var/www/html/index.html
systemctl restart caddy
```
