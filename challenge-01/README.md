server {
    listen         80;
    server_name .algomais.com;
    return 301 https://$host$request_uri;
}

server {
    listen 80;
    listen [::]:80;
    server_name revista.algomais.com;

    return 301 https://algomais.com$request_uri;
}

server {
# Document Root
root /var/www/html;
index index.php index.html index.htm;
server_name .algomais.com;
client_max_body_size 0;

set_real_ip_from 0.0.0.0/0;
set_real_ip_from ::/0;
real_ip_header X-Forwarded-For;

    listen [::]:443 ssl http2 ipv6only=on;
    listen 443 ssl http2;
        ssl_protocols TLSv1.1 TLSv1.2 TLSv1.3;
        ssl_certificate /etc/letsencrypt/live/algomais.com/fullchain.pem;
        ssl_certificate_key /etc/letsencrypt/live/algomais.com/privkey.pem;
        ssl_prefer_server_ciphers on;
        ssl_session_cache   shared:SSL:20m;
        ssl_session_timeout 20m;
        ssl_ciphers 'TLS13+AESGCM+AES128:EECDH+AES128';


error_page 404 /404.html;
error_page 500 502 503 504 /50x.html;

