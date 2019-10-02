### Memcached installation 

Memcached is a chache module 'like redice' 
we can install it directly using brew or pecl (which found by default in php >= 7 versions)

then we should run the memcached service by typing `memcached -d -p 11211` 

this port is the default in my project 'u can check ur project config file' in my case it is in parameters.yml

### Memcached checking 

we can check if memecached is running by  `telnet localhost 11211` if it shows Connected to localhost then yay u :) 

#### Note

Memcached is not recommended to use with token sessions cache , because when the server restart all caches sessions will
be removed so all ur users will be disconnected automatically which is not useful, for this case u can use redice or just use 
the database method (old school method xD)