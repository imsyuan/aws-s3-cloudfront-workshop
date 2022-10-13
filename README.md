# AWS 使用 S3 與 CloudFront 輕鬆架站

## S3 – Lab #1

- 創建 S3 Bucket
- 調整 `package.json`
    ```
    "upload-to-s3": "aws s3 sync build/ s3://{{你的Bucket名稱}}",
    ```
- 新增 AWS Credential 至 `~/.aws/credentials`
- 如有調整資料需要執行以下指令，即可部署至 AWS S3
    ```bash
    npm run build-and-deploy
    ```