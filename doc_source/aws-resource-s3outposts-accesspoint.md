# AWS::S3Outposts::AccessPoint<a name="aws-resource-s3outposts-accesspoint"></a>

The AWS::S3Outposts::AccessPoint resource specifies an access point and associates it with the specified Amazon S3 on Outposts bucket\. For more information, see [Managing data access with Amazon S3 access points](https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-points.html)\.



**Note**  
S3 on Outposts supports only VPC\-style access points\. 

## Syntax<a name="aws-resource-s3outposts-accesspoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-s3outposts-accesspoint-syntax.json"></a>

```
{
  "Type" : "AWS::S3Outposts::AccessPoint",
  "Properties" : {
      "[Bucket](#cfn-s3outposts-accesspoint-bucket)" : String,
      "[Name](#cfn-s3outposts-accesspoint-name)" : String,
      "[Policy](#cfn-s3outposts-accesspoint-policy)" : Json,
      "[VpcConfiguration](#cfn-s3outposts-accesspoint-vpcconfiguration)" : VpcConfiguration
    }
}
```

### YAML<a name="aws-resource-s3outposts-accesspoint-syntax.yaml"></a>

```
Type: AWS::S3Outposts::AccessPoint
Properties: 
  [Bucket](#cfn-s3outposts-accesspoint-bucket): String
  [Name](#cfn-s3outposts-accesspoint-name): String
  [Policy](#cfn-s3outposts-accesspoint-policy): Json
  [VpcConfiguration](#cfn-s3outposts-accesspoint-vpcconfiguration): 
    VpcConfiguration
```

## Properties<a name="aws-resource-s3outposts-accesspoint-properties"></a>

`Bucket`  <a name="cfn-s3outposts-accesspoint-bucket"></a>
The Amazon Resource Name \(ARN\) of the S3 on Outposts bucket that is associated with this access point\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-s3outposts-accesspoint-name"></a>
The name of this access point\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Policy`  <a name="cfn-s3outposts-accesspoint-policy"></a>
The access point policy associated with this access point\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcConfiguration`  <a name="cfn-s3outposts-accesspoint-vpcconfiguration"></a>
The virtual private cloud \(VPC\) configuration for this access point, if one exists\.  
*Required*: Yes  
*Type*: [VpcConfiguration](aws-properties-s3outposts-accesspoint-vpcconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-s3outposts-accesspoint-return-values"></a>

### Ref<a name="aws-resource-s3outposts-accesspoint-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the access point ARN\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-s3outposts-accesspoint-return-values-fn--getatt"></a>

#### <a name="aws-resource-s3outposts-accesspoint-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
This resource contains the details of the S3 on Outposts bucket access point ARN\. This resource is read\-only\.

## Examples<a name="aws-resource-s3outposts-accesspoint--examples"></a>



### Creating an access point with an access point policy for your Amazon S3 on Outposts using CloudFormation<a name="aws-resource-s3outposts-accesspoint--examples--Creating_an_access_point_with_an_access_point_policy_for_your_Amazon_S3_on_Outposts_using_CloudFormation"></a>

The following example shows how you can create an S3 on Outposts bucket and S3 on Outposts access point in the same CFN stack\.

**Note**  
To create an access point, you must already have an S3 on Outposts bucket ARN\. This means that you must create your Outposts bucket before or at the same time as you create the access point\.

#### JSON<a name="aws-resource-s3outposts-accesspoint--examples--Creating_an_access_point_with_an_access_point_policy_for_your_Amazon_S3_on_Outposts_using_CloudFormation--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "Bucket, no tags, no lifecycle configuration with access point",
    "Resources": {
        "ExampleS3OutpostsBucket": {
            "Type": "AWS::S3Outposts::Bucket",
            "Properties": {
                "BucketName": "DOC-EXAMPLE-BUCKET",
                "OutpostID": "op-01ac5d28a6a232904"
            }
        },
        "ExampleS3OutpostsAccessPoint": {
            "Type": "AWS::S3Outposts::AccessPoint",
            "Properties": {
                "Bucket": {
                    "Ref": "ExampleS3OutpostsBucket"
                },
                "Name": "ExampleAccessPoint",
                "VpcConfiguration": {
                    "VpcID": "vpc-12345"
                },
                "Policy": {
                    "Version":"2012-10-17",
                    "ID":"AccessPointPolicy",
                    "Statement":[{
                        "Sid":"st1",
                        "Effect":"Allow",
                        "Principal":{"AWS":"arn:aws:iam::123456789012:root"},
                        "Action":"s3-outposts:*",
                        "Resource": "arn:aws:s3-outposts:us-east-1:123456789012:outpost/op-01ac5d28a6a232904/accesspoint/ExampleAccessPoint"
                    }]
                }
                
            }
        }
    },
    "Outputs": {
        "ExampleS3OutpostsBucketARN": {
            "Description": "The ARN of ExampleS3OutpostsBucket",
            "Value": { "Ref": "ExampleS3OutpostsBucket" }
        },
        "ExampleS3OutpostsAccessPointARN": {
            "Description": "The ARN of ExampleS3OutpostsAccessPoint",
            "Value": {"Ref": "ExampleS3OutpostsAccessPoint" }
        },
        "ExampleS3OutpostsStackID": {
            "Description": "The stack ID",
            "Value": { "Ref": "AWS::StackID" },
            "Export": { "Name": {"Fn::Sub": "${AWS::StackName}-StackID"}}
        }
    }
}
```

#### YAML<a name="aws-resource-s3outposts-accesspoint--examples--Creating_an_access_point_with_an_access_point_policy_for_your_Amazon_S3_on_Outposts_using_CloudFormation--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Description: Bucket, no tags, no lifecycle configuration with access point
Resources:
  ExampleS3OutpostsBucket:
    Type: AWS::S3Outposts::Bucket
    Properties:
      BucketName: DOC-EXAMPLE-BUCKET
      OutpostID: op-01ac5d28a6a232904
  ExampleS3OutpostsAccessPoint:
    Type: AWS::S3Outposts::AccessPoint
    Properties:
      Bucket:
        Ref: ExampleS3OutpostsBucket
      Name: ExampleAccessPoint
      VpcConfiguration:
        VpcID: vpc-12345
      Policy:
        Version: '2012-10-17'
        ID: AccessPointPolicy
        Statement:
        - Sid: st1
          Effect: Allow
          Principal:
            AWS: arn:aws:iam::123456789012:root
          Action: s3-outposts:*
          Resource: arn:aws:s3-outposts:us-east-1:1234567890:outpost/op-01ac5d28a6a232904/accesspoint/ExampleAccessPoint
Outputs:
  ExampleS3OutpostsBucketARN:
    Description: The ARN of ExampleS3OutpostsBucket
    Value:
      Ref: ExampleS3OutpostsBucket
  ExampleS3OutpostsAccessPointARN:
    Description: The ARN of ExampleS3OutpostsAccessPoint
    Value:
      Ref: ExampleS3OutpostsAccessPoint
  ExampleS3OutpostsStackID:
    Description: The stack ID
    Value:
      Ref: AWS::StackID
    Export:
      Name:
        Fn::Sub: "${AWS::StackName}-StackID"
```