#Omeka Installation

Followed general process as outlined in wordpress -
  - download and unzip Omeka Classic file
  - created new database and user for use in mysql
  - added permissions; chown and chmod; owner www-data.
  - sudo apt install imagemagick
  - sudo a2enmod rewrite and add 
      <Directory /var/www/html/omeka>
        Options Indexes FollowSymLinks
        AllowOverride ALL
        Require all granted
      </Directory>

Somehow, still had an 403 Forbidden Error when trying to reach the page. sudo apachectl -S showed it was pulling from root /var/www/omeka despite meant to pull from /var/www/html/omeka
Used sudo a2dissite omeka.conf to disable omeka site 
Used sudo a2ensite 000-default.conf to enable  site 000-default
systemctl restart apache2 then fixed the error
