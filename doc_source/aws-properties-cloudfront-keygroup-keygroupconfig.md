# AWS::CloudFront::KeyGroup KeyGroupConfig<a name="aws-properties-cloudfront-keygroup-keygroupconfig"></a>

A key group configuration\.

A key group contains a list of public keys that you can use with [CloudFront signed URLs and signed cookies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PrivateContent.html)\.

## Syntax<a name="aws-properties-cloudfront-keygroup-keygroupconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-keygroup-keygroupconfig-syntax.json"></a>

```
{
  "[Comment](#cfn-cloudfront-keygroup-keygroupconfig-comment)" : String,
  "[Items](#cfn-cloudfront-keygroup-keygroupconfig-items)" : [ String, ... ],
  "[Name](#cfn-cloudfront-keygroup-keygroupconfig-name)" : String
}
```

### YAML<a name="aws-properties-cloudfront-keygroup-keygroupconfig-syntax.yaml"></a>

```
  [Comment](#cfn-cloudfront-keygroup-keygroupconfig-comment): String
  [Items](#cfn-cloudfront-keygroup-keygroupconfig-items): 
    - String
  [Name](#cfn-cloudfront-keygroup-keygroupconfig-name): String
```

## Properties<a name="aws-properties-cloudfront-keygroup-keygroupconfig-properties"></a>

`Comment`  <a name="cfn-cloudfront-keygroup-keygroupconfig-comment"></a>
A comment to describe the key group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Items`  <a name="cfn-cloudfront-keygroup-keygroupconfig-items"></a>
A list of the identifiers of the public keys in the key group\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-cloudfront-keygroup-keygroupconfig-name"></a>
A name to identify the key group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)