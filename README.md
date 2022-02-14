# Gitaction Frontend Deploy

There're serveral stages:

- setup enviroments, such like nodejs
- yarn install and build
- sync to aws s3 (would open CDN usually)
- zip and sync to aws server
- restart nginx service (defaults to use nginx)

## Usage

```yaml
- uses: dogedefi/gitaction-frontend-deploy@master
    with:
    AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
    AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
    AWS_BUCKET_NAME: 'sandbox.relation.network'
    AWS_TARGET: 'relation_website'
    PROJECT: relation_website
    DEPLOY_KEY: ${{ secrets.RELATION_WEB_AWS_DEPLOY_KEY }}
    SSH_SERVER: ${{ secrets.RELATION_WEB_AWS_SSH_SERVER }}
    SSH_ROOT: ${{ secrets.RELATION_WEB_AWS_SSH_ROOT }}
```
