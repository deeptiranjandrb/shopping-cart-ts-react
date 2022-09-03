This project is built using react and typescript.
This project is bootstrapped using vite.
# shopping-cart-ts-react

# steps for deployment to s3 using access key
- create a iam user with only permission to s3 bucket
- enable public access to the bucket and attach a public access resource policy to the bucket(Ref: https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteAccessPermissionsReqd.html)
- store the access credentials for the iam user in git secrets for the repository
- create your deploy yml file in .github/workflows

Ref for deployment: https://backbencher.dev/articles/deploy-react-app-amazon-s3-github-actions

# steps for deployment to s3 using assumeRole
- add github OIDC as a identity provider in aws
- create a role for web identity and select identity provider as github and audience as sts
- attach required policy to the role
- change the trust relationship condition to restrict useage of the role.
- change in the yml file
- publish

Ref for deployment: 
- https://grrr.tech/posts/2021/github-actions-assume-role/
- https://docs.github.com/en/actions/deployment/security-hardening-your-deployments/configuring-openid-connect-in-amazon-web-services