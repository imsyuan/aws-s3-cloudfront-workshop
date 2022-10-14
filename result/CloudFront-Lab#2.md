# CloudFront – Lab #2 Steps

## Steps

- Enter AWS CloudFront
    - Create distribution
        - Origin domain
            - find your S3 bucket
        - Save
    - Edit behavior
        - `Viewer`
            - Redirect HTTP to HTTPS
        - `Cache key and origin requests`
            - Cache policy and origin request policy (recommended)
            - CachingDisabled
        - Save
- Check CloudFront working or not
    - Distributions
        - Distribution domain name
        - `https://d1cd80lzuxtilm.cloudfront.net`
        - Make sure everything is perfect
