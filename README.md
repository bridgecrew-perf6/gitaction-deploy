# Gitaction Frontend Deploy

There're serveral stages:

- setup enviroments, such like nodejs
- yarn install and build
- sync to aws s3 (would open CDN usually)
- zip and sync to aws server
- restart nginx service (defaults to use nginx)
