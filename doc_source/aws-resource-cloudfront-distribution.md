# AWS::CloudFront::Distribution<a name="aws-resource-cloudfront-distribution"></a>

Creates an Amazon CloudFront web distribution\. For general information about CloudFront distributions, see the [Introduction to Amazon CloudFront](http://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html) in the *Amazon CloudFront Developer Guide*\. For specific information about creating CloudFront web distributions, see [CreateDistribution](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CreateDistribution.html) in the *Amazon CloudFront API Reference*\.

**Topics**
+ [Syntax](#aws-resource-cloudfront-distribution-syntax)
+ [Properties](#aws-resource-cloudfront-distribution-prop)
+ [Return Values](#aws-resource-cloudfront-distribution-ref)
+ [Example](#aws-resource-cloudfront-distribution-examples)
+ [See Also](#aws-resource-cloudfront-distribution-seealso)

## Syntax<a name="aws-resource-cloudfront-distribution-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudfront-distribution-syntax.json"></a>

```
{
   "Type" : "AWS::CloudFront::Distribution",
   "Properties" : {
      "[DistributionConfig](#cfn-cloudfront-distribution-distributionconfig)" : [*DistributionConfig*](aws-properties-cloudfront-distribution-distributionconfig.md),
      "[Tags](#cfn-cloudfront-distribution-tags)" : [ [*Tag*](aws-properties-cloudfront-streamingdistribution-tag.md), ... ]
   }
}
```

### YAML<a name="aws-resource-cloudfront-distribution-syntax.yaml"></a>

```
Type: "AWS::CloudFront::Distribution"
Properties:
  [DistributionConfig](#cfn-cloudfront-distribution-distributionconfig): 
    [*DistributionConfig*](aws-properties-cloudfront-distribution-distributionconfig.md)
  [Tags](#cfn-cloudfront-distribution-tags): 
    - [*Tag*](aws-properties-cloudfront-streamingdistribution-tag.md)
```

## Properties<a name="aws-resource-cloudfront-distribution-prop"></a>

`DistributionConfig`  <a name="cfn-cloudfront-distribution-distributionconfig"></a>
The distribution's configuration information\.  
*Required*: Yes  
*Type*: [DistributionConfig](aws-properties-cloudfront-distribution-distributionconfig.md) type  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Tags`  <a name="cfn-cloudfront-distribution-tags"></a>
An arbitrary set of tags \(key–value pairs\) to associate with a CloudFront distribution\.  
 *Required*: No  
 *Type*: List of [](aws-properties-cloudfront-streamingdistribution-tag.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)   
Duplicates not allowed\.

## Return Values<a name="aws-resource-cloudfront-distribution-ref"></a>

### Ref<a name="w3ab2c21c10d215c11b2"></a>

*Returns*: The CloudFront distribution ID\. For example: `E27LVI50CSW06W`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d215c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`DomainName`  
*Returns*: The domain name of the resource\. For example: `d2fadu0nynjpfn.cloudfront.net`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Example<a name="aws-resource-cloudfront-distribution-examples"></a>

### <a name="aws-resource-cloudfront-distribution-example1"></a>

The following example specifies a distribution and assigns it a single tag\.

#### JSON<a name="aws-resource-cloudfront-distribution-example1.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "cloudfrontdistribution": {
            "Type": "AWS::CloudFront::Distribution",
            "Properties": {
                "DistributionConfig": {
                    "CacheBehaviors": [
                        {
                            "LambdaFunctionAssociations": [
                                {
                                    "EventType": "string-value",
                                    "LambdaFunctionARN": "string-value"
                                }
                            ]
                        }
                    ],
                    "DefaultCacheBehavior": {
                        "LambdaFunctionAssociations": [
                            {
                                "EventType": "string-value",
                                "LambdaFunctionARN": "string-value"
                            }
                        ]
                    },
                    "IPV6Enabled": "boolean-value",
                    "Origins": [
                        {
                            "CustomOriginConfig": {
                                "OriginKeepaliveTimeout": "integer-value",
                                "OriginReadTimeout": "integer-value"
                            }
                        }
                    ]
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

#### YAML<a name="aws-resource-cloudfront-distribution-example1.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  cloudfrontdistribution:
    Type: 'AWS::CloudFront::Distribution'
    Properties:
      DistributionConfig:
        CacheBehaviors:
          - LambdaFunctionAssociations:
              - EventType: string-value
                LambdaFunctionARN: string-value
        DefaultCacheBehavior:
          LambdaFunctionAssociations:
            - EventType: string-value
              LambdaFunctionARN: string-value
        IPV6Enabled: boolean-value
        Origins:
          - CustomOriginConfig:
              OriginKeepaliveTimeout: integer-value
              OriginReadTimeout: integer-value
      Tags:
        - Key: string-value
          Value: string-value
```

## See Also<a name="aws-resource-cloudfront-distribution-seealso"></a>
+ [CreateDistribution](http://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CreateDistribution.html) in the *Amazon CloudFront API Reference*