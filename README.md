# turbo-octo-train

System requirements for development:

Node
```
node -v

v14.15.4
``

AWS CLI
```
aws --version

aws-cli/2.1.1 Python/3.7.4 Darwin/20.2.0 exe/x86_64
```

Serverless framework
```
serverless -v 

Framework Core: 2.19.0
Plugin: 4.4.2
SDK: 2.3.2
Components: 3.4.7
```

## Invoke function

Local invocation of hello function
```
sls invoke local --function hello
{
    "statusCode": 200,
    "body": "{\n  \"message\": \"Go Serverless v1.0! Your function executed successfully!\",\n  \"input\": {}\n}"
}
```

Invoke deployes lambda function in AWS

```
curl -X POST --location "https://9lb6eobeqd.execute-api.us-east-1.amazonaws.com/dev/hello"
```

```
POST https://9lb6eobeqd.execute-api.us-east-1.amazonaws.com/dev/hello

HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 20
Connection: keep-alive
Date: Sun, 17 Jan 2021 13:46:46 GMT
x-amzn-RequestId: 12d89eac-c820-4f41-82c2-4adb6482a4e9
x-amz-apigw-id: ZS7nCGbkoAMFnuw=
X-Amzn-Trace-Id: Root=1-60043fc6-3c6ec3c32d6dc2bb3b25315a;Sampled=0
X-Cache: Miss from cloudfront
Via: 1.1 828a61ebc3af4e0465a5577a4c08af7b.cloudfront.net (CloudFront)
X-Amz-Cf-Pop: ARN54-C1
X-Amz-Cf-Id: zSrG4Ibx643egOluuedjxQSwYiB6c9cTWJeXINqdMdukfeHFP_3kiw==

"Hello from Lambda!"

Response code: 200 (OK); Time: 784ms; Content length: 20 bytes
```