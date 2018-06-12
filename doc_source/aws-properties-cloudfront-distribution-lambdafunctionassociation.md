# Amazon CloudFront Distribution LambdaFunctionAssociation<a name="aws-properties-cloudfront-distribution-lambdafunctionassociation"></a>

<a name="aws-properties-cloudfront-distribution-lambdafunctionassociation-description"></a>The `LambdaFunctionAssociation` property type specifies a Lambda function association for an Amazon CloudFront distribution\.

<a name="aws-properties-cloudfront-distribution-lambdafunctionassociation-inheritance"></a> `LambdaFunctionAssociation` is a property of the [CloudFront Distribution CacheBehavior](aws-properties-cloudfront-distribution-cachebehavior.md) and [CloudFront Distribution DefaultCacheBehavior](aws-properties-cloudfront-distribution-defaultcachebehavior.md) property types\. 

## Syntax<a name="aws-properties-cloudfront-distribution-lambdafunctionassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-distribution-lambdafunctionassociation-syntax.json"></a>

```
{
  "[EventType](#cfn-cloudfront-distribution-lambdafunctionassociation-eventtype)" : String,
  "[LambdaFunctionARN](#cfn-cloudfront-distribution-lambdafunctionassociation-lambdafunctionarn)" : String
}
```

### YAML<a name="aws-properties-cloudfront-distribution-lambdafunctionassociation-syntax.yaml"></a>

```
[EventType](#cfn-cloudfront-distribution-lambdafunctionassociation-eventtype): String
[LambdaFunctionARN](#cfn-cloudfront-distribution-lambdafunctionassociation-lambdafunctionarn): String
```

## Properties<a name="aws-properties-cloudfront-distribution-lambdafunctionassociation-properties"></a>

`EventType`  <a name="cfn-cloudfront-distribution-lambdafunctionassociation-eventtype"></a>
Specifies the event type that triggers a Lambda function invocation\. For valid values and definitions, see [LambdaFunctionAssociation](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_LambdaFunctionAssociation.html) in the *Amazon CloudFront API Reference*\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`LambdaFunctionARN`  <a name="cfn-cloudfront-distribution-lambdafunctionassociation-lambdafunctionarn"></a>
The ARN of the Lambda function\. You must specify the ARN of a function version; you can't specify a Lambda alias or $LATEST\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-cloudfront-distribution-lambdafunctionassociation-seealso"></a>
+ [LambdaFunctionAssociation](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_LambdaFunctionAssociation.html) in the *Amazon CloudFront API Reference*