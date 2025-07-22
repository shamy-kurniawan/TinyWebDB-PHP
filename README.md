1. Goto apache directory Ex:
   `cd /var/www/htm`
   Download the files :
   `wget https://github.com/shamy-kurniawan/TinyWebDB-PHP/archive/refs/heads/master.zip`
   Extract the files :
   `unzip master.zip`
   rename directory (optional for eazy)
   `mv TinyWebDB-PHP-master database`
   Goto directory
   `cd dataabse`
   change you permission file database.
   `sudo chmod 666 database.json`
   cek the directory for now
   `pwd` and ex answer `/var/www/html/database` that mine you address tinywebdb in https://you-domain.is/database

2. Configure the apache server
   edit the apache file config
   `sudo nano /etc/apache2/apache2.conf`
   find the rules like `Directory /var/www/html>` the change like this :
   `<Directory /var/www/legends>
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
    </Directory> `
   then save it
   
3. execute command for apply change
   `sudo a2enmod rewrite`
    `sudo systemctl restart apache2`

5.  Ex of block:
     ![image|690x252](https://github.com/shamy-kurniawan/TinyWebDB-PHP/blob/master/blocks.png)
    
7.  Done
   
