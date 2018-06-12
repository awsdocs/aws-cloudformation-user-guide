# Amazon CloudFront StreamingDistribution Tag<a name="aws-properties-cloudfront-streamingdistribution-tag"></a>

<a name="aws-properties-cloudfront-streamingdistribution-tag-description"></a>The `Tag` property type specifies key\-value pairs for an Amazon CloudFront streaming distribution\.

<a name="aws-properties-cloudfront-streamingdistribution-tag-inheritance"></a> `Tag` is a property of the [AWS::CloudFront::StreamingDistribution](aws-resource-cloudfront-streamingdistribution.md) resource type\. 

## Syntax<a name="aws-properties-cloudfront-streamingdistribution-tag-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudfront-streamingdistribution-tag-syntax.json"></a>

```
{
  "[Key](#cfn-cloudfront-streamingdistribution-tag-key)" : String,
  "[Value](#cfn-cloudfront-streamingdistribution-tag-value)" : String
}
```

### YAML<a name="aws-properties-cloudfront-streamingdistribution-tag-syntax.yaml"></a>

```
[Key](#cfn-cloudfront-streamingdistribution-tag-key): String
[Value](#cfn-cloudfront-streamingdistribution-tag-value): String
```

## Properties<a name="aws-properties-cloudfront-streamingdistribution-tag-properties"></a>

`Key`  <a name="cfn-cloudfront-streamingdistribution-tag-key"></a>
A string that contains `Tag` key\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Value`  <a name="cfn-cloudfront-streamingdistribution-tag-value"></a>
A string that contains an optional `Tag` value\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-cloudfront-streamingdistribution-seealso"></a>
+ [Tag](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_Tag.html) in the *Amazon CloudFront API Reference*