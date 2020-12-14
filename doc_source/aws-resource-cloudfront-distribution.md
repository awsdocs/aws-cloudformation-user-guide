# AWS::CloudFront::Distribution<a name="aws-resource-cloudfront-distribution"></a>

A distribution tells CloudFront where you want content to be delivered from, and the details about how to track and manage content delivery\.

## Syntax<a name="aws-resource-cloudfront-distribution-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudfront-distribution-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFront::Distribution",
  "Properties" : {
      "[DistributionConfig](#cfn-cloudfront-distribution-distributionconfig)" : DistributionConfig,
      "[Tags](#cfn-cloudfront-distribution-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-cloudfront-distribution-syntax.yaml"></a>

```
Type: AWS::CloudFront::Distribution
Properties: 
  [DistributionConfig](#cfn-cloudfront-distribution-distributionconfig): 
    DistributionConfig
  [Tags](#cfn-cloudfront-distribution-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-cloudfront-distribution-properties"></a>

`DistributionConfig`  <a name="cfn-cloudfront-distribution-distributionconfig"></a>
The current configuration information for the distribution\. Send a `GET` request to the `/CloudFront API version/distribution ID/config` resource\.  
*Required*: Yes  
*Type*: [DistributionConfig](aws-properties-cloudfront-distribution-distributionconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-cloudfront-distribution-tags"></a>
A complex type that contains zero or more `Tag` elements\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cloudfront-distribution-return-values"></a>

### Ref<a name="aws-resource-cloudfront-distribution-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the CloudFront distribution ID\. For example: `E27LVI50CSW06W`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cloudfront-distribution-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudfront-distribution-return-values-fn--getatt-fn--getatt"></a>

`DomainName`  <a name="DomainName-fn::getatt"></a>
The domain name of the resource, such as `d111111abcdef8.cloudfront.net`\.

## Examples<a name="aws-resource-cloudfront-distribution--examples"></a>



### Create a distribution<a name="aws-resource-cloudfront-distribution--examples--Create_a_distribution"></a>

The following example specifies a distribution and assigns it a single tag\.

#### JSON<a name="aws-resource-cloudfront-distribution--examples--Create_a_distribution--json"></a>

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

#### YAML<a name="aws-resource-cloudfront-distribution--examples--Create_a_distribution--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  cloudfrontdistribution:
    Type: AWS::CloudFront::Distribution
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

## See also<a name="aws-resource-cloudfront-distribution--seealso"></a>
+  [CreateDistribution](https://docs.aws.amazon.com/cloudfront/latest/APIReference/API_CreateDistribution.html) in the *Amazon CloudFront API Reference* 

