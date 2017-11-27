# Installation
Put nginx folder and docker-compose.yml file in your symfony's project files.

Command to execute :
- docker-compose run --rm php composer install --prefer-dist --no-progress --no-suggest
- docker-compose up -d --remove-orphans
- docker-compose exec php chmod -R 777 /app/var

# To use with dnsdock

##Mac
- sudo route -n add -net 172.31.200.0 192.168.99.100
- echo 'nameserver 172.31.200.1' | sudo tee /etc/resolver/tld > /dev/null

##Linux
- Install resolvconf
- Add 'nameserver 172.31.200.1' to /etc/resolvconf/resolv.conf.d/head
