# Streamdata.io GitHub Users Search Streaming to AWS S3 Data Lake (Serverless)
<img src="https://s3.amazonaws.com/kinlane-productions/streamdata/streamdata-logo-vertical-2.png" align="right" width="250" />This is a demo of delivering a stream of Github users searches using Streamdata.io running on AWS Lambda as a "serverless" function. It is designed to take this existing JSON API and turn it into a streaming API using Server-Sent Events (SSE), applying incremental updates using JSON Patch, and then stream the results into a data lake store on Amazon S3.

You will need a Streamdata.io account and application key to run this function, as well as an AWS account to run the Lambda function in, and AWS S3 to store the data. You can run this as stream for up to five minutes (the maximum timeout of a Lambda script), then rerun every X minutes, or other schedule using AWS CloudWatch Events. Providing an existing API stream that can be turned on or off as needed, delivering real time updates to your Amazon S3 data lake.

## Key Links:
- [Streamdata.io Service](http://streamdata.io)
- [Streamdata.io Account Signup](https://portal.streamdata.io/)
- [GitHub API](https://developer.github.com/v3/activity/events/)
- [AWS Serverless Application Repository](https://serverlessrepo.aws.amazon.com/#/applications/arn:aws:serverlessrepo:us-east-1:879370021840:applications~streamdata-io-github-search-users)
- [License: MIT License](https://github.com/streamdata-serverless/streamdata-io-github-userss-search/blob/master/LICENSE)

## Frequently Asked Questions:

- Is an API key needed? Yes, you will need a GitHub OAuth token, which you can find under your Github account under your personal developer tokens.
- Where does the data end up in Amazon S3? There are two environment variables for the function: 1) s3bucket, and 2) targetFolder, which will define your "data lake" destination on Amazon S3 -- you will need to create the bucket, but the folder will automatically be created.
- Where do I get support for this function? Submit your userss via [the Github repository for this project](https://github.com/streamdata-serverless/streamdata-io-github-userss-search/userss)
