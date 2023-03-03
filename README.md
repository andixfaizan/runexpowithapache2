# run expo with apache2

```
sudo apt install apache2
```

```
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
```

```
sudo apt-get install nodejs
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
npm run build
```

```
cd /var/www/html
```
```
rm -r index.html
```
```
cd
```
```
cd sayangwe
```


```
cp -r dist /var/www/html
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

