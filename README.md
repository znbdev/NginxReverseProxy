# Nginx reverse proxy

This is a simple example of how to set up a reverse proxy using Nginx and Docker.

# Usage

### Before starting the Docker container, run the following command to initially obtain the SSL certificate

```shell
docker-compose run --rm certbot certonly --webroot --webroot-path=/var/www/certbot --email your-email@example.com --agree-tos --no-eff-email -d yourdomain.com
```

### Make sure to replace yourdomain.com with your domain name and your-email@example.com with your email address.

### Start the Docker container
Run the following commands to start the Nginx and Certbot containers
```shell
docker-compose up -d
```

### Visit your domain and you should see the Nginx server's welcome page.
[yourdomain.com](https://yourdomain.com)
