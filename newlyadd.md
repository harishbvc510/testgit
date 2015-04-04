==========to pass requeust port 8080 from 80===========
packages: sudo a2enmod proxy proxy_http
open vim /etc/http/conf/sites-available/jenkins.conf/sites-available/jenkins.conf
</VirtualHost *:80>
ServerName host.allinone.com
ProxyRequeust off
<Proxy *>
Order deny,allow
Allow from all
</Proxy>
proxyPreserverhost on
proxyPass / http://host.allinone.com:8080/
</VirtualHost>
