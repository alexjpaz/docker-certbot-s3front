# docker-certbot-s3front

```
docker run \
   -e AWS_SECRET_ACCESS_KEY="$AWS_SECRET_ACCESS_KEY" \
   -e AWS_ACCESS_KEY_ID="$AWS_ACCESS_KEY_ID" \
    t \
    certbot --agree-tos -a certbot-s3front:auth \
    --non-interactive \
    --email $EMAIL \
    --certbot-s3front:auth-s3-bucket $S3_BUCKET_NAME \
    -i certbot-s3front:installer \
    --certbot-s3front:installer-cf-distribution-id $CLOUDFRONT_ID \
    -d $DOMAIN_NAME
```
