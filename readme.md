This project is built using react and typescript.
This project is bootstrapped using vite.
# shopping-cart-ts-react

# steps for deployment to s3 
- create a iam user with only permission to s3 bucket
- enable public access to the bucket and attach a public access resource policy to the bucket(Ref: https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteAccessPermissionsReqd.html)
- store the access credentials for the iam user in git secrets for the repository
- create your deploy yml file in .github/workflows

Ref for deployment: https://backbencher.dev/articles/deploy-react-app-amazon-s3-github-actions