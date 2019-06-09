# arm64v8-docker-certbot-cert-updater

### Update all the certs for all the domains using a certbot container and jenkins.

This assumes that your build container can mount to the appropriate cert directories.

I've got all of mine on a file share that jenkins can reach, so my volume mapping looks like this:  

/mnt/fileshare/certbot/conf:/etc/letsencrypt  
/mnt/fileshare/certbot/www:/var/www/certbot  
