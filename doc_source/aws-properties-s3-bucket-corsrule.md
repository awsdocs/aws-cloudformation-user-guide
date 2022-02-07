# AWS::S3::Bucket CorsRule<a name="aws-properties-s3-bucket-corsrule"></a>

Specifies a cross\-origin access rule for an Amazon S3 bucket\.

## Syntax<a name="aws-properties-s3-bucket-corsrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-corsrule-syntax.json"></a>

```
{
  "[AllowedHeaders](#cfn-s3-bucket-corsrule-allowedheaders)" : [ String, ... ],
  "[AllowedMethods](#cfn-s3-bucket-corsrule-allowedmethods)" : [ String, ... ],
  "[AllowedOrigins](#cfn-s3-bucket-corsrule-allowedorigins)" : [ String, ... ],
  "[ExposedHeaders](#cfn-s3-bucket-corsrule-exposedheaders)" : [ String, ... ],
  "[Id](#cfn-s3-bucket-corsrule-id)" : String,
  "[MaxAge](#cfn-s3-bucket-corsrule-maxage)" : Integer
}
```

### YAML<a name="aws-properties-s3-bucket-corsrule-syntax.yaml"></a>

```
  [AllowedHeaders](#cfn-s3-bucket-corsrule-allowedheaders): 
    - String
  [AllowedMethods](#cfn-s3-bucket-corsrule-allowedmethods): 
    - String
  [AllowedOrigins](#cfn-s3-bucket-corsrule-allowedorigins): 
    - String
  [ExposedHeaders](#cfn-s3-bucket-corsrule-exposedheaders): 
    - String
  [Id](#cfn-s3-bucket-corsrule-id): String
  [MaxAge](#cfn-s3-bucket-corsrule-maxage): Integer
```

## Properties<a name="aws-properties-s3-bucket-corsrule-properties"></a>

`AllowedHeaders`  <a name="cfn-s3-bucket-corsrule-allowedheaders"></a>
Headers that are specified in the `Access-Control-Request-Headers` header\. These headers are allowed in a preflight OPTIONS request\. In response to any preflight OPTIONS request, Amazon S3 returns any requested headers that are allowed\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowedMethods`  <a name="cfn-s3-bucket-corsrule-allowedmethods"></a>
An HTTP method that you allow the origin to run\.  
*Allowed values*: `GET` \| `PUT` \| `HEAD` \| `POST` \| `DELETE`  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowedOrigins`  <a name="cfn-s3-bucket-corsrule-allowedorigins"></a>
One or more origins you want customers to be able to access the bucket from\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExposedHeaders`  <a name="cfn-s3-bucket-corsrule-exposedheaders"></a>
One or more headers in the response that you want customers to be able to access from their applications \(for example, from a JavaScript `XMLHttpRequest` object\)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-s3-bucket-corsrule-id"></a>
A unique identifier for this rule\. The value must be no more than 255 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxAge`  <a name="cfn-s3-bucket-corsrule-maxage"></a>
The time in seconds that your browser is to cache the preflight response for the specified resource\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-s3-bucket-corsrule--examples"></a>



### Enable cross\-origin resource sharing<a name="aws-properties-s3-bucket-corsrule--examples--Enable_cross-origin_resource_sharing"></a>

The following example template shows a public S3 bucket with two cross\-origin resource sharing rules\.

#### JSON<a name="aws-properties-s3-bucket-corsrule--examples--Enable_cross-origin_resource_sharing--json"></a>

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

#### YAML<a name="aws-properties-s3-bucket-corsrule--examples--Enable_cross-origin_resource_sharing--yaml"></a>

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