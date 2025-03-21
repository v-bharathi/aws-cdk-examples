# Amazon Api Gateway Rest Api to Amazon SQS

This example creates a rest api together with a SQS. By calling the rest api, a message will be forwarded to the SQS.

## Deploy
Run `cdk deploy`. This will deploy / redeploy your Stack to your AWS Account.

## Testing

Obtain Resource ID
```
$ aws apigateway get-resources --rest-api-id <Rest API ID>
```

Test the endpoint
```
$ aws apigateway test-invoke-method --rest-api-id <Rest API ID> --resource-id <RESOURCE ID> --http-method POST --body {"key":"value"}
```

## Synthesize Cloudformation Template
To see the Cloudformation template generated by the CDK, run `cdk synth`, then check the output file in the "cdk.out" directory.
