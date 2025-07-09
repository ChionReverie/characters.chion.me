# characters.chion.me

This is a jekyll site!


To update the site:
```bash
cd _site && \ 
s3cmd --no-mime-magic --acl-public --delete-removed --delete-after sync . s3://chion-characters
```
