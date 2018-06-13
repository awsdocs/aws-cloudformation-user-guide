# AWS::CloudFront::StreamingDistribution<a name="aws-resource-cloudfront-streamingdistribution"></a>

The `AWS::CloudFront::StreamingDistribution` resource specifies an RMTP distribution for Amazon CloudFront\. An RTMP distribution is similar to a web distribution, but an RTMP distribution streams media files using the Adobe Real\-Time Messaging Protocol \(RTMP\) instead of serving files using HTTP\. For more information, see [CreateStreamingDistribution](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CreateStreamingDistribution.html) in the *Amazon CloudFront API Reference*\. 

**Topics**
+ [Syntax](#aws-resource-cloudfront-streamingdistribution-syntax)
+ [Properties](#aws-resource-cloudfront-streamingdistribution-properties)
+ [Return Values](#aws-resource-cloudfront-streamingdistribution-returnvalues)
+ [Example](#aws-resource-cloudfront-streamingdistribution-examples)
+ [See Also](#aws-resource-cloudfront-streamingdistribution-seealso)

## Syntax<a name="aws-resource-cloudfront-streamingdistribution-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudfront-streamingdistribution-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFront::StreamingDistribution",
  "Properties" : {
    "[StreamingDistributionConfig](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig)" : [*StreamingDistributionConfig*](aws-properties-cloudfront-streamingdistribution-streamingdistributionconfig.md),
    "[Tags](#cfn-cloudfront-streamingdistribution-tags)" : [ [*Tag*](aws-properties-cloudfront-streamingdistribution-tag.md), ... ]
  }
}
```

### YAML<a name="aws-resource-cloudfront-streamingdistribution-syntax.yaml"></a>

```
Type: "AWS::CloudFront::StreamingDistribution"
Properties:
  [StreamingDistributionConfig](#cfn-cloudfront-streamingdistribution-streamingdistributionconfig): StreamingDistributionConfig
  [Tags](#cfn-cloudfront-streamingdistribution-tags): 
    - [*Tag*](aws-properties-cloudfront-streamingdistribution-tag.md)
```

## Properties<a name="aws-resource-cloudfront-streamingdistribution-properties"></a>

`StreamingDistributionConfig`  <a name="cfn-cloudfront-streamingdistribution-streamingdistributionconfig"></a>
Information about the configuration of the RMTP streaming distribution\.  
 *Required*: Yes  
 *Type*: [CloudFront StreamingDistribution StreamingDistributionConfig](aws-properties-cloudfront-streamingdistribution-streamingdistributionconfig.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Tags`  <a name="cfn-cloudfront-streamingdistribution-tags"></a>
Key\-value tags to assign to this streaming distribution\.  
 *Required*: Yes  
 *Type*: List of [CloudFront StreamingDistribution Tag](aws-properties-cloudfront-streamingdistribution-tag.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)   
Duplicates not allowed\.

## Return Values<a name="aws-resource-cloudfront-streamingdistribution-returnvalues"></a>

### Ref<a name="w3ab2c21c10d223c12b3"></a>

When you pass the logical ID of an `AWS::CloudFront::StreamingDistribution` resource to the intrinsic `Ref` function, the function returns the streaming distribution ID, such as `E1E7FEN9T35R9W`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="w3ab2c21c10d223c12b5"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`DomainName`  
The domain name of the resource, such as `sct27g85mgx04.cloudfront.net`\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Example<a name="aws-resource-cloudfront-streamingdistribution-examples"></a>

### <a name="aws-resource-cloudfront-streamingdistribution-example1"></a>

The following example specifies a streaming distribution and assigns it a single tag\.

#### JSON<a name="aws-resource-cloudfront-streamingdistribution-example1.json"></a>

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

#### YAML<a name="aws-resource-cloudfront-streamingdistribution-example1.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  streamingdistribution:
    Type: 'AWS::CloudFront::StreamingDistribution'
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

## See Also<a name="aws-resource-cloudfront-streamingdistribution-seealso"></a>
+ [CreateStreamingDistribution](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CreateStreamingDistribution.html) in the *Amazon CloudFront API Reference*