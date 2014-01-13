apps
======================

Page speed app instalation and configuration for Nginx

Git Nginx Pagespeed App

    mkdir /etc/nginx/apps
    cd /etc/nginx/apps
    git clone https://github.com/Coozila/apps
    
Update Nginx Pagespeed App

    cd /etc/nginx/apps
    git pull
    
Add Pagespeed app to your server block

    ## HTTP server.
    server {
    listen 80; # IPv4
    ## Replace the IPv6 address by your own address. The address below
    ## was stolen from the wikipedia page on IPv6.
    #listen [fe80::202:b3ff:fe1e:8330]:80 ipv6only=on;


    server_name test.yursite.com;


    ## Access and error logs.


    access_log /var/log/nginx/test.yoursite.com/test.yoursite.com_access.log;
    error_log /var/log/nginx/test.yoursite.com/test.yoursite.com_error.log;


    ###########################################################################
    ## Nginx Pagespeed App 										
    ###########################################################################
    include apps/pagespeed/ngx_pagespeed.conf;


etc...
