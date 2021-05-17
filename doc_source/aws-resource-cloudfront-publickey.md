# AWS::CloudFront::PublicKey<a name="aws-resource-cloudfront-publickey"></a>

A public key that you can use with [signed URLs and signed cookies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PrivateContent.html), or with [field\-level encryption](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/field-level-encryption.html)\.

## Syntax<a name="aws-resource-cloudfront-publickey-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudfront-publickey-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFront::PublicKey",
  "Properties" : {
      "[PublicKeyConfig](#cfn-cloudfront-publickey-publickeyconfig)" : PublicKeyConfig
    }
}
```

### YAML<a name="aws-resource-cloudfront-publickey-syntax.yaml"></a>

```
Type: AWS::CloudFront::PublicKey
Properties: 
  [PublicKeyConfig](#cfn-cloudfront-publickey-publickeyconfig): 
    PublicKeyConfig
```

## Properties<a name="aws-resource-cloudfront-publickey-properties"></a>

`PublicKeyConfig`  <a name="cfn-cloudfront-publickey-publickeyconfig"></a>
Configuration information about a public key that you can use with [signed URLs and signed cookies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PrivateContent.html), or with [field\-level encryption](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/field-level-encryption.html)\.  
*Required*: Yes  
*Type*: [PublicKeyConfig](aws-properties-cloudfront-publickey-publickeyconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cloudfront-publickey-return-values"></a>

### Ref<a name="aws-resource-cloudfront-publickey-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the public key\. For example: `K36X4X2EO997HM`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cloudfront-publickey-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudfront-publickey-return-values-fn--getatt-fn--getatt"></a>

`CreatedTime`  <a name="CreatedTime-fn::getatt"></a>
The date and time when the public key was uploaded\.

`Id`  <a name="Id-fn::getatt"></a>
The identifier of the public key\.