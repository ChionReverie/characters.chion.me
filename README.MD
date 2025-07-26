# chion.me

This is a jekyll site!

## Cloudflare Site Setup

This guidance should only really matter for Chion, the owner of the site.

Prerequisites:
* Install AWS CLI
* Set up an R2 bucket in Cloudflare. (In this case, `chion-dot-me` is the name of the bucket).
* Set `CLOUDFLARE_R2_ENDPOINT` environment variable to the endpoint of the bucket.

To update the site:
```bash
cd _site && \
aws s3 --endpoint-url ${CLOUDFLARE_R2_ENDPOINT} sync . s3://chion-dot-me --acl public-read --delete
```
