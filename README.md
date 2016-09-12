RewriteCond %{HTTP_HOST} ^www\.(.+)$ [NC]
RewriteRule ^ http://%1%{REQUEST_URI} [L,R=301]

RewriteCond %{THE_REQUEST} ^[A-Z]{3,9}\ /index\.html\ HTTP/
RewriteRule ^index\.html$ / [R=301,L]
RewriteCond %{THE_REQUEST} ^[A-Z]{3,9}\ /index\.php\ HTTP/
RewriteRule ^index\.php$ / [R=301,L]