quickstart
==========

`quickstart` is a barebones PHP application, set up with common web development
frameworks, which you can quickly clone or copy to jump straight into a new web project.

# Features

1. Coffeescript is compiled into Javascript (from `site/js/`)
2. SCSS is compiled into CSS (from `site/css/`)
3. HAML is compiled into HTML using templates (from `site/templates/`)
4. CSS images are spritified using [spritify](https://github.com/soundasleep/spritify)

# Using

1. [Fork this project](https://github.com/soundasleep/quickstart) or
   [download the latest .zip](https://github.com/soundasleep/quickstart/archive/master.zip).
2. Update the package descriptions in `package.json` and `composer.json`
3. Run `npm install` and `composer update`
4. Edit your pages in `site/` as necessary
5. Edit `inc/global.php` to define your `absolute_url` and any necessary CSS/JS includes (e.g. JQuery)
6. If using Apache, edit `site/.htaccess` to set your `REWRITEBASE`
7. Run `grunt` to compile the assets. (You can also use `grunt serve` to watch for changes.)

# Deploying

## Apache 2.4

```conf
<VirtualHost *:80>
  ServerName openclerk.org
  ServerAlias www.openclerk.org
  DocumentRoot /var/www/openclerk.org/site/
  <Directory /var/www/openclerk.org/site/>
    AllowOverride all
  </Directory>
</VirtualHost>
```
