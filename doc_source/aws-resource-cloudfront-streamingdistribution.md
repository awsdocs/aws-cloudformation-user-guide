# AWS::CloudFront::StreamingDistribution<a name="aws-resource-cloudfront-streamingdistribution"></a>

This resource is deprecated\. Amazon CloudFront is deprecating real\-time messaging protocol \(RTMP\) distributions on December 31, 2020\. For more information, [read the announcement](http://forums.aws.amazon.com/ann.jspa?annID=7356) on the Amazon CloudFront discussion forum\.

## Syntax<a name="aws-resource-cloudfront-streamingdistribution-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudfront-streamingdistribution-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFront::StreamingDistribution",
  "Properties" : {
      "[StreamingDistributionConfig](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig)" : StreamingDistributionConfig,
      "[Tags](#cfn-cloudfront-streamingdistribution-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-cloudfront-streamingdistribution-syntax.yaml"></a>

```
Type: AWS::CloudFront::StreamingDistribution
Properties: 
  [StreamingDistributionConfig](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig): 
    StreamingDistributionConfig
  [Tags](#cfn-cloudfront-streamingdistribution-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-cloudfront-streamingdistribution-properties"></a>

`StreamingDistributionConfig`  <a name="cfn-cloudfront-streamingdistribution-streamingdistributionconfig"></a>
The current configuration information for the RTMP distribution\.  
*Required*: Yes  
*Type*: [StreamingDistributionConfig](aws-properties-cloudfront-streamingdistribution-streamingdistributionconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-cloudfront-streamingdistribution-tags"></a>
A complex type that contains zero or more `Tag` elements\.  
*Required*: Yes  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cloudfront-streamingdistribution-return-values"></a>

### Ref<a name="aws-resource-cloudfront-streamingdistribution-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the streaming distribution ID, such as `E1E7FEN9T35R9W`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cloudfront-streamingdistribution-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudfront-streamingdistribution-return-values-fn--getatt-fn--getatt"></a>

`DomainName`  <a name="DomainName-fn::getatt"></a>
The domain name of the resource, such as `d111111abcdef8.cloudfront.net`\.