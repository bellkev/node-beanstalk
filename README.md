# node-beanstalk

This is a simple example of deploying a nodejs application from CircleCI to AWS Elastic Beanstalk. Follow the instructions below to get started.

**Create an S3 bucket:**
- Create an s3 bucket with whatever name you like to transfer code to elastic beanstalk

**Setup Elastic Beanstalk:**
- Create an application
- Create web server environment for node.js (single instance is fine for demo purposes)
- You can start with the sample application (you'll deploy your own from CircleCI later)
- Choose any environment name you like
- Skip/proceed through the rest of the setup

**Setup CircleCI project settings:**
- Configure AWS credentials at `https://circleci.com/gh/{org name}/{project name}/edit#aws` (must be able to access the s3 bucket and the beanstalk app)
- Add the following environment variables at `https://circleci.com/gh/{org name}/{project name}/edit#env-vars`:
  - EB_BUCKET: The s3 bucket you set up earlier
  - EB_APP: The name of the beanstalk app
  - EB_ENV: The name of the beanstalk environment to deploy to
  - AWS_DEFAULT_REGION: The region of your app

Once you've done all that, try deploying, making some changes, and deploying some more! You can also try breaking the test by removing/changing the text "Congratulations" in `index.html`.
