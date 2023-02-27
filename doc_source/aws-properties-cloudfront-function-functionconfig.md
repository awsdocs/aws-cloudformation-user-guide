# AWS::CloudFront::Function FunctionConfig<a name="aws-properties-cloudfront-function-functionconfig"></a>

Contains configuration information about a CloudFront function\.

## Syntax<a name="aws-properties-cloudfront-function-functionconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-function-functionconfig-syntax.json"></a>

```
{
  "[Comment](#cfn-cloudfront-function-functionconfig-comment)" : String,
  "[Runtime](#cfn-cloudfront-function-functionconfig-runtime)" : String
}
```

### YAML<a name="aws-properties-cloudfront-function-functionconfig-syntax.yaml"></a>

```
  [Comment](#cfn-cloudfront-function-functionconfig-comment): String
  [Runtime](#cfn-cloudfront-function-functionconfig-runtime): String
```

## Properties<a name="aws-properties-cloudfront-function-functionconfig-properties"></a>

`Comment`  <a name="cfn-cloudfront-function-functionconfig-comment"></a>
A comment to describe the function\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Runtime`  <a name="cfn-cloudfront-function-functionconfig-runtime"></a>
The function's runtime environment\. The only valid value is `cloudfront-js-1.0`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `cloudfront-js-1.0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)