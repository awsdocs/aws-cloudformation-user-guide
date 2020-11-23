# AWS::CloudFront::StreamingDistribution<a name="aws-resource-cloudfront-streamingdistribution"></a>

A streaming distribution tells CloudFront where you want RTMP content to be delivered from, and the details about how to track and manage content delivery\.

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

## Examples<a name="aws-resource-cloudfront-streamingdistribution--examples"></a>

### Create a streaming distribution<a name="aws-resource-cloudfront-streamingdistribution--examples--Create_a_streaming_distribution"></a>

The following example specifies a streaming distribution and assigns it a single tag\.

#### JSON<a name="aws-resource-cloudfront-streamingdistribution--examples--Create_a_streaming_distribution--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "streamingdistribution": {
            "Type": "AWS::CloudFront::StreamingDistribution",
            "Properties": {
                "StreamingDistributionConfig": {
                    "Aliases": [
                        "string-values"
                    ],
                    "Comment": "string-value",
                    "Enabled": "boolean-value",
                    "Logging": {
                        "Bucket": "string-value",
                        "Enabled": "boolean-value",
                        "Prefix": "string-value"
                    },
                    "PriceClass": "string-value",
                    "S3Origin": {
                        "DomainName": "string-value",
                        "OriginAccessIdentity": "string-value"
                    },
                    "TrustedSigners": {
                        "Enabled": "boolean-value",
                        "AwsAccountNumbers": [
                            "string-values"
                        ]
                    }
                },
                "Tags": [
                    {
                        "Key": "string-value",
                        "Value": "string-value"
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-cloudfront-streamingdistribution--examples--Create_a_streaming_distribution--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  streamingdistribution:
    Type: AWS::CloudFront::StreamingDistribution
    Properties:
      StreamingDistributionConfig:
        Aliases:
          - string-values
        Comment: string-value
        Enabled: boolean-value
        Logging:
          Bucket: string-value
          Enabled: boolean-value
          Prefix: string-value
        PriceClass: string-value
        S3Origin:
          DomainName: string-value
          OriginAccessIdentity: string-value
        TrustedSigners:
          Enabled: boolean-value
          AwsAccountNumbers:
            - string-values
      Tags:
        - Key: string-value
          Value: string-value
```