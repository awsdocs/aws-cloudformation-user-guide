# AWS Lambda\-backed custom resources<a name="template-custom-resources-lambda"></a>

When you associate a Lambda function with a custom resource, the function is invoked whenever the custom resource is created, updated, or deleted\.  AWS CloudFormation calls a Lambda API to invoke the function and to pass all the request data \(such as the request type and resource properties\) to the function\. The power and customizability of Lambda functions in combination with AWS CloudFormation enable a wide range of scenarios, such as dynamically looking up AMI IDs during stack creation, or implementing and using utility functions, such as string reversal functions\.

**Topics**
+ [Walkthrough: Looking up Amazon Machine Image IDs](walkthrough-custom-resources-lambda-lookup-amiids.md)
+ [`cfn-response` module](cfn-lambda-function-code-cfnresponsemodule.md)