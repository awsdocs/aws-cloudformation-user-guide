# AWS::CloudFront::StreamingDistribution TrustedSigners<a name="aws-properties-cloudfront-streamingdistribution-trustedsigners"></a>

A list of AWS accounts whose public keys CloudFront can use to verify the signatures of signed URLs and signed cookies\.

## Syntax<a name="aws-properties-cloudfront-streamingdistribution-trustedsigners-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-streamingdistribution-trustedsigners-syntax.json"></a>

```
{
  "[AwsAccountNumbers](#cfn-cloudfront-streamingdistribution-trustedsigners-awsaccountnumbers)" : [ String, ... ],
  "[Enabled](#cfn-cloudfront-streamingdistribution-trustedsigners-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-cloudfront-streamingdistribution-trustedsigners-syntax.yaml"></a>

```
  [AwsAccountNumbers](#cfn-cloudfront-streamingdistribution-trustedsigners-awsaccountnumbers): 
    - String
  [Enabled](#cfn-cloudfront-streamingdistribution-trustedsigners-enabled): Boolean
```

## Properties<a name="aws-properties-cloudfront-streamingdistribution-trustedsigners-properties"></a>

`AwsAccountNumbers`  <a name="cfn-cloudfront-streamingdistribution-trustedsigners-awsaccountnumbers"></a>
An AWS account number that contains active CloudFront key pairs that CloudFront can use to verify the signatures of signed URLs and signed cookies\. If the AWS account that owns the key pairs is the same account that owns the CloudFront distribution, the value of this field is `self`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-cloudfront-streamingdistribution-trustedsigners-enabled"></a>
This field is `true` if any of the AWS accounts have public keys that CloudFront can use to verify the signatures of signed URLs and signed cookies\. If not, this field is `false`\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-cloudfront-streamingdistribution-trustedsigners--seealso"></a>
+  [TrustedSigners](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_TrustedSigners.html) in the *Amazon CloudFront API Reference* 

