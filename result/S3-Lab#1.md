# S3 – Lab #1 Steps

## Steps

- Enter AWS S3
    - Create your bucket
    - Type your bucket name: `steven-lab1`
    - Uncheck `Block all public access`
    - Create bucket
- Clone Github Repo
    - Update `package.json`
        ```
        "upload-to-s3": "aws s3 sync build/ s3://{{ steven-lab1 }}",
        ```
    - Add AWS Credential to `~/.aws/credentials`
    - Update your code and deploy code to your S3
        ```bash
        npm run build-and-deploy
        ```
- Find your bucket `steven-lab1`
    - Click tab `Permissions`
    - `Bucket policy` click `Edit` and put the policy
        ```bash
        {
            "Version": "2012-10-17",
            "Statement": [
                {
                    "Sid": "PublicReadGetObject",
                    "Effect": "Allow",
                    "Principal": "*",
                    "Action": "s3:GetObject",
                    "Resource": "arn:aws:s3:::{{ steven-lab1 }}/*"
                }
            ]
        }
        ```
    - Save