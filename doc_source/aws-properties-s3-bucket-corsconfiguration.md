# AWS::S3::Bucket CorsConfiguration<a name="aws-properties-s3-bucket-corsconfiguration"></a>

Describes the cross\-origin access configuration for objects in an Amazon S3 bucket\. For more information, see [Enabling Cross\-Origin Resource Sharing](https://docs.aws.amazon.com/AmazonS3/latest/dev/cors.html) in the *Amazon S3 User Guide*\.

## Syntax<a name="aws-properties-s3-bucket-corsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-corsconfiguration-syntax.json"></a>

```
{
  "[CorsRules](#cfn-s3-bucket-corsconfiguration-corsrules)" : [ CorsRule, ... ]
}
```

### YAML<a name="aws-properties-s3-bucket-corsconfiguration-syntax.yaml"></a>

```
  [CorsRules](#cfn-s3-bucket-corsconfiguration-corsrules): 
    - CorsRule
```

## Properties<a name="aws-properties-s3-bucket-corsconfiguration-properties"></a>

`CorsRules`  <a name="cfn-s3-bucket-corsconfiguration-corsrules"></a>
A set of origins and methods \(cross\-origin access that you want to allow\)\. You can add up to 100 rules to the configuration\.  
*Required*: Yes  
*Type*: List of [CorsRule](aws-properties-s3-bucket-corsrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-s3-bucket-corsconfiguration--examples"></a>



### Enable cross\-origin resource sharing<a name="aws-properties-s3-bucket-corsconfiguration--examples--Enable_cross-origin_resource_sharing"></a>

The following example template shows a public S3 bucket with two cross\-origin resource sharing rules\.

#### JSON<a name="aws-properties-s3-bucket-corsconfiguration--examples--Enable_cross-origin_resource_sharing--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "S3Bucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "AccessControl": "PublicRead",
                "CorsConfiguration": {
                    "CorsRules": [
                        {
                            "AllowedHeaders": [
                                "*"
                            ],
                            "AllowedMethods": [
                                "GET"
                            ],
                            "AllowedOrigins": [
                                "*"
                            ],
                            "ExposedHeaders": [
                                "Date"
                            ],
                            "Id": "myCORSRuleId1",
                            "MaxAge": 3600
                        },
                        {
                            "AllowedHeaders": [
                                "x-amz-*"
                            ],
                            "AllowedMethods": [
                                "DELETE"
                            ],
                            "AllowedOrigins": [
                                "http://www.example.com",
                                "http://www.example.net"
                            ],
                            "ExposedHeaders": [
                                "Connection",
                                "Server",
                                "Date"
                            ],
                            "Id": "myCORSRuleId2",
                            "MaxAge": 1800
                        }
                    ]
                }
            }
        }
    },
    "Outputs": {
        "BucketName": {
            "Value": {
                "Ref": "S3Bucket"
            },
            "Description": "Name of the sample Amazon S3 bucket with CORS enabled."
        }
    }
}
```

#### YAML<a name="aws-properties-s3-bucket-corsconfiguration--examples--Enable_cross-origin_resource_sharing--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  S3Bucket:
    Type: 'AWS::S3::Bucket'
    Properties:
      AccessControl: PublicRead
      CorsConfiguration:
        CorsRules:
          - AllowedHeaders:
              - '*'
            AllowedMethods:
              - GET
            AllowedOrigins:
              - '*'
            ExposedHeaders:
              - Date
            Id: myCORSRuleId1
            MaxAge: 3600
          - AllowedHeaders:
              - x-amz-*
            AllowedMethods:
              - DELETE
            AllowedOrigins:
              - 'http://www.example.com'
              - 'http://www.example.net'
            ExposedHeaders:
              - Connection
              - Server
              - Date
            Id: myCORSRuleId2
            MaxAge: 1800
Outputs:
  BucketName:
    Value: !Ref S3Bucket
    Description: Name of the sample Amazon S3 bucket with CORS enabled.
```