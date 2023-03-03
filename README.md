# run expo with apache2

```
sudo apt install apache2
```

```
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
```

```
sudo apt-get install -y nodejs
```

```
git clone https://github.com/andixfaizan/sayangwe
```

```
cd sayangwe
```

```
npm i
```
```
npm install -g npm@9.6.0
```

```
npm run build
```

```
cp -r dist /var/www/html
```

```
cd /var/www/html
```
```
rm -r index.html
```

```
mv dist/* .
```

```
cd /var/www/html
```
```
cd /etc/apache2/sites-available/
```


```
nano expo.conf
```

```
<VirtualHost *:80>
ServerName www.sendawacoffe.my.id
 ServerAdmin webmaster@www.sendawacoffe.my.id
 DocumentRoot /var/www/html/build
<Directory /var/www/html/build>
  Options Indexes FollowSymLinks MultiViews
  AllowOverride all
  Order Deny,Allow
  Allow from all
  Require all granted
 </Directory>
</VirtualHost>
```




```
systemctl restart apache2.service
```


ssl instakk

```
snap install core; sudo snap refresh core
```

```
snap install --classic certbot ;  ln -s /snap/bin/certbot /usr/bin/certbot
```

```
certbot --apache -d managementexpo.web.id
```
```
/etc/init.d/htt
```

