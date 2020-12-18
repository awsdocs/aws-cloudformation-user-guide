# AWS::CloudFront::Distribution LambdaFunctionAssociation<a name="aws-properties-cloudfront-distribution-lambdafunctionassociation"></a>

A complex type that contains a Lambda function association\.

## Syntax<a name="aws-properties-cloudfront-distribution-lambdafunctionassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-distribution-lambdafunctionassociation-syntax.json"></a>

```
{
  "[EventType](#cfn-cloudfront-distribution-lambdafunctionassociation-eventtype)" : String,
  "[IncludeBody](#cfn-cloudfront-distribution-lambdafunctionassociation-includebody)" : Boolean,
  "[LambdaFunctionARN](#cfn-cloudfront-distribution-lambdafunctionassociation-lambdafunctionarn)" : String
}
```

### YAML<a name="aws-properties-cloudfront-distribution-lambdafunctionassociation-syntax.yaml"></a>

```
  [EventType](#cfn-cloudfront-distribution-lambdafunctionassociation-eventtype): String
  [IncludeBody](#cfn-cloudfront-distribution-lambdafunctionassociation-includebody): Boolean
  [LambdaFunctionARN](#cfn-cloudfront-distribution-lambdafunctionassociation-lambdafunctionarn): String
```

## Properties<a name="aws-properties-cloudfront-distribution-lambdafunctionassociation-properties"></a>

`EventType`  <a name="cfn-cloudfront-distribution-lambdafunctionassociation-eventtype"></a>
Specifies the event type that triggers a Lambda function invocation\. You can specify the following values:  
+  `viewer-request`: The function executes when CloudFront receives a request from a viewer and before it checks to see whether the requested object is in the edge cache\. 
+  `origin-request`: The function executes only when CloudFront sends a request to your origin\. When the requested object is in the edge cache, the function doesn't execute\.
+  `origin-response`: The function executes after CloudFront receives a response from the origin and before it caches the object in the response\. When the requested object is in the edge cache, the function doesn't execute\.
+  `viewer-response`: The function executes before CloudFront returns the requested object to the viewer\. The function executes regardless of whether the object was already in the edge cache\.

  If the origin returns an HTTP status code other than HTTP 200 \(OK\), the function doesn't execute\.
*Required*: No  
*Type*: String  
*Allowed values*: `origin-request | origin-response | viewer-request | viewer-response`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeBody`  <a name="cfn-cloudfront-distribution-lambdafunctionassociation-includebody"></a>
A flag that allows a Lambda function to have read access to the body content\. For more information, see [Accessing the Request Body by Choosing the Include Body Option](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/lambda-include-body-access.html) in the Amazon CloudFront Developer Guide\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LambdaFunctionARN`  <a name="cfn-cloudfront-distribution-lambdafunctionassociation-lambdafunctionarn"></a>
The ARN of the Lambda function\. You must specify the ARN of a function version; you can't specify a Lambda alias or $LATEST\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-cloudfront-distribution-lambdafunctionassociation--seealso"></a>
+  [LambdaFunctionAssociation](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_LambdaFunctionAssociation.html) in the *Amazon CloudFront API Reference* 

