# laravel-502-bad-gateway

1. Add the following in Nginx configuration file `/etc/nginx/nginx.conf`

```
location ~ \.php$ {
    ...
    fastcgi_buffers 16 16k;
    fastcgi_buffer_size 32k;
    ...
}
```

2. Restart Nginx
`sudo systemctl restart nginx`
