# AWS::S3::Bucket CorsConfiguration<a name="aws-properties-s3-bucket-cors"></a>

Describes the cross\-origin access configuration for objects in an Amazon S3 bucket\. For more information, see [Enabling Cross\-Origin Resource Sharing](https://docs.aws.amazon.com/AmazonS3/latest/dev/cors.html) in the *Amazon Simple Storage Service Developer Guide*\.

## Syntax<a name="aws-properties-s3-bucket-cors-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-cors-syntax.json"></a>

```
{
  "[CorsRules](#cfn-s3-bucket-cors-corsrule)" : [ CorsRule, ... ]
}
```

### YAML<a name="aws-properties-s3-bucket-cors-syntax.yaml"></a>

```
  [CorsRules](#cfn-s3-bucket-cors-corsrule): 
    - CorsRule
```

## Properties<a name="aws-properties-s3-bucket-cors-properties"></a>

`CorsRules`  <a name="cfn-s3-bucket-cors-corsrule"></a>
A set of origins and methods \(cross\-origin access that you want to allow\)\. You can add up to 100 rules to the configuration\.  
*Required*: Yes  
*Type*: List of [CorsRule](aws-properties-s3-bucket-cors-corsrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-s3-bucket-cors--seealso"></a>
+ AWS::S3::Bucket [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html#aws-properties-s3-bucket--examples)

