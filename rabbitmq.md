Ubuntu
------

## Client 
http://www.rabbitmq.com/download.html

## Server
```command
sudo apt-get update
sudo apt-get install php5-dev
git clone git://github.com/alanxz/rabbitmq-c.git cd rabbitmq-c 
git submodule init 
git submodule update 
autoreconf -i 
./configure 
make
sudo make install
sudo pecl install amqp
sudo touch /etc/php5/mods-available/amqp.ini  
echo "extension=amqp.so" | sudo tee -a /etc/php5/mods-available/amqp.ini
sudo php5enmod amqp 
php -r "phpinfo();" | grep amqp
sudo invoke-rc.d rabbitmq-server start
```

##Web ui
```command
sudo rabbitmq-plugins enable rabbitmq_management
sudo service rabbit-server restart
http://127.0.0.1:15672
```

Default user/pass : guest/guest | change password

##STOMP adapter
```command
rabbitmq-plugins enable rabbitmq_stomp
sudo service rabbit-server restart
```