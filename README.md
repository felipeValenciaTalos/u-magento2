### Install

1. `composer install`

1. Edit your hosts file
`127.0.0.1 local.u-magento2.com`

1. Edit your apache vhosts file
```
<VirtualHost [your namevirtualhost]>
   ServerName local.u-magento2.com
   ServerAdmin webmaster@localhost
   SetEnv MAGE_MODE developer
   php_value error_reporting 1
   php_flag display_errors on
   DocumentRoot [path-to-u-magento2-folder]
   <Directory [path-to-u-magento2-folder]>
      Options FollowSymLinks
      AllowOverride All
      Order allow,deny
      allow from all
   </Directory>
</VirtualHost>  
```

1. Create database
`CREATE DATABASE u_magento2_2_1_5 CHARACTER SET utf8 COLLATE utf8_general_ci;` 

1. Import database
`mysql -u youruser -p u_magento2_2_1_5 < import 2_1_5.sql`

1. Copy `app/etc/env.php.sample` to `app/etc/env.php`
Update your database settings

1. Copy `app/etc/config.php.sample` to `app/etc/config.php`


### Magento Admin Info
- Username: admin
- Email: admin@example.com
- Password: magento123

- Store URL: http://local.u-magento2.com/2_1_5/
- Store Admin URL: http://local.u-magento2.com/2_1_5/admin/

