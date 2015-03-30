Ubuntu
------

```command
sudo apt-get install libevent-dev
pecl install channel://pecl.php.net/libevent-0.0.5
sudo touch /etc/php5/mods-available/libevent.ini
echo "extension=libevent.so" | sudo tee -a /etc/php5/mods-available/libevent.ini
sudo php5enmod libevent
php -r "phpinfo();" | grep libevent
```