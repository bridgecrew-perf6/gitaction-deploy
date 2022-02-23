# Deploy Node to AWS

There're serveral stages:

- setup enviroments, such like nodejs
- yarn install and build
- zip and sync to aws server
- restart nginx service (defaults to use nginx)

## Usage

```yaml
- uses: dogedefi/gitaction-deploy/aws-node@master
    with:
    AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
    AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
    PROJECT: relation_website
    DEPLOY_KEY: ${{ secrets.RELATION_WEB_AWS_DEPLOY_KEY }}
    SSH_SERVER: ${{ secrets.RELATION_WEB_AWS_SSH_SERVER }}
    SSH_ROOT: ${{ secrets.RELATION_WEB_AWS_SSH_ROOT }}
```
