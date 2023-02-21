# AWS::CloudFront::ContinuousDeploymentPolicy SingleHeaderConfig<a name="aws-properties-cloudfront-continuousdeploymentpolicy-singleheaderconfig"></a>

Determines which HTTP requests are sent to the staging distribution\.

## Syntax<a name="aws-properties-cloudfront-continuousdeploymentpolicy-singleheaderconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-continuousdeploymentpolicy-singleheaderconfig-syntax.json"></a>

```
{
  "[Header](#cfn-cloudfront-continuousdeploymentpolicy-singleheaderconfig-header)" : String,
  "[Value](#cfn-cloudfront-continuousdeploymentpolicy-singleheaderconfig-value)" : String
}
```

### YAML<a name="aws-properties-cloudfront-continuousdeploymentpolicy-singleheaderconfig-syntax.yaml"></a>

```
  [Header](#cfn-cloudfront-continuousdeploymentpolicy-singleheaderconfig-header): String
  [Value](#cfn-cloudfront-continuousdeploymentpolicy-singleheaderconfig-value): String
```

## Properties<a name="aws-properties-cloudfront-continuousdeploymentpolicy-singleheaderconfig-properties"></a>

`Header`  <a name="cfn-cloudfront-continuousdeploymentpolicy-singleheaderconfig-header"></a>
The request header name that you want CloudFront to send to your staging distribution\. The header must contain the prefix `aws-cf-cd-`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-cloudfront-continuousdeploymentpolicy-singleheaderconfig-value"></a>
The request header value\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)