# AWS::CloudFront::PublicKey PublicKeyConfig<a name="aws-properties-cloudfront-publickey-publickeyconfig"></a>

Configuration information about a public key that you can use with [signed URLs and signed cookies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PrivateContent.html), or with [field\-level encryption](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/field-level-encryption.html)\.

## Syntax<a name="aws-properties-cloudfront-publickey-publickeyconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-publickey-publickeyconfig-syntax.json"></a>

```
{
  "[CallerReference](#cfn-cloudfront-publickey-publickeyconfig-callerreference)" : String,
  "[Comment](#cfn-cloudfront-publickey-publickeyconfig-comment)" : String,
  "[EncodedKey](#cfn-cloudfront-publickey-publickeyconfig-encodedkey)" : String,
  "[Name](#cfn-cloudfront-publickey-publickeyconfig-name)" : String
}
```

### YAML<a name="aws-properties-cloudfront-publickey-publickeyconfig-syntax.yaml"></a>

```
  [CallerReference](#cfn-cloudfront-publickey-publickeyconfig-callerreference): String
  [Comment](#cfn-cloudfront-publickey-publickeyconfig-comment): String
  [EncodedKey](#cfn-cloudfront-publickey-publickeyconfig-encodedkey): String
  [Name](#cfn-cloudfront-publickey-publickeyconfig-name): String
```

## Properties<a name="aws-properties-cloudfront-publickey-publickeyconfig-properties"></a>

`CallerReference`  <a name="cfn-cloudfront-publickey-publickeyconfig-callerreference"></a>
A string included in the request to help make sure that the request can’t be replayed\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Comment`  <a name="cfn-cloudfront-publickey-publickeyconfig-comment"></a>
A comment to describe the public key\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncodedKey`  <a name="cfn-cloudfront-publickey-publickeyconfig-encodedkey"></a>
The public key that you can use with [signed URLs and signed cookies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PrivateContent.html), or with [field\-level encryption](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/field-level-encryption.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-cloudfront-publickey-publickeyconfig-name"></a>
A name to help identify the public key\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)