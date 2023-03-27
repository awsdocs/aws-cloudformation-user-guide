# AWS::S3::AccessPoint<a name="aws-resource-s3-accesspoint"></a>

The AWS::S3::AccessPoint resource is an Amazon S3 resource type that you can use to access buckets\.

## Syntax<a name="aws-resource-s3-accesspoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-s3-accesspoint-syntax.json"></a>

```
{
  "Type" : "AWS::S3::AccessPoint",
  "Properties" : {
      "[Bucket](#cfn-s3-accesspoint-bucket)" : String,
      "[BucketAccountId](#cfn-s3-accesspoint-bucketaccountid)" : String,
      "[Name](#cfn-s3-accesspoint-name)" : String,
      "[Policy](#cfn-s3-accesspoint-policy)" : Json,
      "[PolicyStatus](#cfn-s3-accesspoint-policystatus)" : PolicyStatus,
      "[PublicAccessBlockConfiguration](#cfn-s3-accesspoint-publicaccessblockconfiguration)" : PublicAccessBlockConfiguration,
      "[VpcConfiguration](#cfn-s3-accesspoint-vpcconfiguration)" : VpcConfiguration
    }
}
```

### YAML<a name="aws-resource-s3-accesspoint-syntax.yaml"></a>

```
Type: AWS::S3::AccessPoint
Properties: 
  [Bucket](#cfn-s3-accesspoint-bucket): String
  [BucketAccountId](#cfn-s3-accesspoint-bucketaccountid): String
  [Name](#cfn-s3-accesspoint-name): String
  [Policy](#cfn-s3-accesspoint-policy): Json
  [PolicyStatus](#cfn-s3-accesspoint-policystatus): 
    PolicyStatus
  [PublicAccessBlockConfiguration](#cfn-s3-accesspoint-publicaccessblockconfiguration): 
    PublicAccessBlockConfiguration
  [VpcConfiguration](#cfn-s3-accesspoint-vpcconfiguration): 
    VpcConfiguration
```

## Properties<a name="aws-resource-s3-accesspoint-properties"></a>

`Bucket`  <a name="cfn-s3-accesspoint-bucket"></a>
The name of the bucket associated with this access point\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BucketAccountId`  <a name="cfn-s3-accesspoint-bucketaccountid"></a>
The AWS account ID associated with the S3 bucket associated with this access point\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-s3-accesspoint-name"></a>
The name of this access point\. If you don't specify a name, AWS CloudFormation generates a unique ID and uses that ID for the access point name\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Policy`  <a name="cfn-s3-accesspoint-policy"></a>
The access point policy associated with this access point\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyStatus`  <a name="cfn-s3-accesspoint-policystatus"></a>
The container element for a bucket's policy status\.  
*Required*: No  
*Type*: [PolicyStatus](aws-properties-s3-accesspoint-policystatus.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PublicAccessBlockConfiguration`  <a name="cfn-s3-accesspoint-publicaccessblockconfiguration"></a>
The PublicAccessBlock configuration that you want to apply to this Amazon S3 bucket\. You can enable the configuration options in any combination\. For more information about when Amazon S3 considers a bucket or object public, see [The Meaning of "Public"](https://docs.aws.amazon.com/AmazonS3/latest/dev/access-control-block-public-access.html#access-control-block-public-access-policy-status) in the *Amazon S3 User Guide*\.   
*Required*: No  
*Type*: [PublicAccessBlockConfiguration](aws-properties-s3-accesspoint-publicaccessblockconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcConfiguration`  <a name="cfn-s3-accesspoint-vpcconfiguration"></a>
The Virtual Private Cloud \(VPC\) configuration for this access point, if one exists\.  
*Required*: No  
*Type*: [VpcConfiguration](aws-properties-s3-accesspoint-vpcconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-s3-accesspoint-return-values"></a>

### Ref<a name="aws-resource-s3-accesspoint-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the access point name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-s3-accesspoint-return-values-fn--getatt"></a>

#### <a name="aws-resource-s3-accesspoint-return-values-fn--getatt-fn--getatt"></a>

`Alias`  <a name="Alias-fn::getatt"></a>
The alias for this access point\.

`Arn`  <a name="Arn-fn::getatt"></a>
This property contains the details of the ARN for the access point\.

`Name`  <a name="Name-fn::getatt"></a>
The name of this access point\.

`NetworkOrigin`  <a name="NetworkOrigin-fn::getatt"></a>
Indicates whether this access point allows access from the internet\. If `VpcConfiguration` is specified for this access point, then `NetworkOrigin` is `VPC`, and the access point doesn't allow access from the internet\. Otherwise, `NetworkOrigin` is `Internet`, and the access point allows access from the internet, subject to the access point and bucket access policies\.  
*Allowed values*: `VPC` \| `Internet` 

## Examples<a name="aws-resource-s3-accesspoint--examples"></a>



### Create an S3 Access Point<a name="aws-resource-s3-accesspoint--examples--Create_an_S3_Access_Point"></a>

The following example creates an Amazon S3 access point for the given S3 bucket\. This access point allows user `JaneDoe` to make GetObject and PutObject operations only for bucket objects prefixed with `/janedoe`\. You must include `/object` in the resource ARN path\.

For more information, see [Configuring IAM policies for using access points](https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-points-policies.html) and [Managing and using access points](https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-access-points.html) in the *Amazon S3 User Guide*\.

#### JSON<a name="aws-resource-s3-accesspoint--examples--Create_an_S3_Access_Point--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "S3Bucket": {
            "Type": "AWS::S3::Bucket"
        },
        "S3BucketPolicy": {
            "Type": "AWS::S3::BucketPolicy",
            "Properties": {
                "Bucket": {
                    "Ref": "S3Bucket"
                },
                "PolicyDocument": {
                    "Version": "2012-10-17",
                    "Statement": [
                        {
                            "Action": "*",
                            "Effect": "Allow",
                            "Resource": [
                                {
                                    "Fn::GetAtt": [
                                        "S3Bucket",
                                        "Arn"
                                    ]
                                },
                                {
                                    "Fn::Join": [
                                        "",
                                        [
                                            {
                                                "Fn::GetAtt": [
                                                    "S3Bucket",
                                                    "Arn"
                                                ]
                                            },
                                            "/*"
                                        ]
                                    ]
                                }
                            ],
                            "Principal": {
                                "AWS": "*"
                            },
                            "Condition": {
                                "StringEquals": {
                                    "s3:DataAccessPointAccount": {
                                        "Ref": "AWS::AccountId"
                                    }
                                }
                            }
                        }
                    ]
                }
            }
        },
        "S3AccessPoint": {
            "Type": "AWS::S3::AccessPoint",
            "Properties": {
                "Bucket": {
                    "Ref": "S3Bucket"
                },
                "Name": "my-access-point",
                "Policy": {
                    "Version": "2012-10-17",
                    "Statement": [
                        {
                            "Action": [
                                "s3:GetObject",
                                "s3:PutObject"
                            ],
                            "Effect": "Allow",
                            "Resource": [
                                {
                                    "Fn::Sub": "arn:${AWS::Partition}:s3:${AWS::Region}:${AWS::AccountId}:accesspoint/my-access-point/object/janedoe/*"
                                }
                            ],
                            "Principal": {
                                "AWS": {
                                    "Fn::Sub": "arn:${AWS::Partition}:iam::${AWS::AccountId}:user/JaneDoe"
                                }
                            }
                        }
                    ]
                }
            }
        }
    },
   "Outputs": {
        "S3AccessPointArn": {
            "Value": {
                "Fn::GetAtt": ["S3AccessPoint", "Arn"]
            },
            "Description": "ARN of the sample Amazon S3 access point."
        },
        "S3AccessPointName": {
            "Value": {
                "Fn::GetAtt": ["S3AccessPoint", "Name"]
            },
            "Description": "Name of the sample Amazon S3 access point."
        },
        "S3AccessPointAlias": {
            "Value": {
                "Fn::GetAtt": ["S3AccessPoint", "Alias"]
            },
            "Description": "Alias of the sample Amazon S3 access point."
        }
    }
}
```

#### YAML<a name="aws-resource-s3-accesspoint--examples--Create_an_S3_Access_Point--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  S3Bucket:
    Type: 'AWS::S3::Bucket'
  S3BucketPolicy:
    Type: 'AWS::S3::BucketPolicy'
    Properties:
      Bucket: !Ref S3Bucket
      PolicyDocument:
        Version: 2012-10-17
        Statement:
          - Action: '*'
            Effect: Allow
            Resource:
              - !GetAtt
                - S3Bucket
                - Arn
              - !Join
                - ''
                - - !GetAtt
                    - S3Bucket
                    - Arn
                  - /*
            Principal:
              AWS: '*'
            Condition:
              StringEquals:
                's3:DataAccessPointAccount': !Ref 'AWS::AccountId'
  S3AccessPoint:
    Type: 'AWS::S3::AccessPoint'
    Properties:
      Bucket: !Ref S3Bucket
      Name: my-access-point
      Policy:
        Version: 2012-10-17
        Statement:
          - Action:
              - 's3:GetObject'
              - 's3:PutObject'
            Effect: Allow
            Resource:
               - !Sub  'arn:${AWS::Partition}:s3:${AWS::Region}:${AWS::AccountId}:accesspoint/my-access-point/object/janedoe/*'
            Principal:
              AWS: !Sub 'arn:${AWS::Partition}:iam::${AWS::AccountId}:user/JaneDoe'
Outputs:
  S3AccessPointArn:
    Value:
      Fn::GetAtt:
      - S3AccessPoint
      - Arn
    Description: ARN of the sample Amazon S3 access point.
  S3AccessPointName:
    Value:
      Fn::GetAtt:
      - S3AccessPoint
      - Name
    Description: Name of the sample Amazon S3 access point.
  S3AccessPointAlias:
    Value:
      Fn::GetAtt:
      - S3AccessPoint
      - Alias
    Description: Alias of the sample Amazon S3 access point.
```

### Create an S3 Access Point restricted to a VPC<a name="aws-resource-s3-accesspoint--examples--Create_an_S3_Access_Point_restricted_to_a_VPC"></a>

The following example creates an Amazon S3 access point restricted to a virtual private cloud \(VPC\)\. For more information, see [Configuring IAM policies for using access points](https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-points-policies.html) in the *Amazon S3 User Guide*\.

#### JSON<a name="aws-resource-s3-accesspoint--examples--Create_an_S3_Access_Point_restricted_to_a_VPC--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "S3Bucket": {
            "Type": "AWS::S3::Bucket"
        },
        "S3BucketPolicy": {
            "Type": "AWS::S3::BucketPolicy",
            "Properties": {
                "Bucket": {
                    "Ref": "S3Bucket"
                },
                "PolicyDocument": {
                    "Version": "2012-10-17",
                    "Statement": [
                        {
                            "Action": "*",
                            "Effect": "Allow",
                            "Resource": [
                                {
                                    "Fn::GetAtt": [
                                        "S3Bucket",
                                        "Arn"
                                    ]
                                },
                                {
                                    "Fn::Join": [
                                        "",
                                        [
                                            {
                                                "Fn::GetAtt": [
                                                    "S3Bucket",
                                                    "Arn"
                                                ]
                                            },
                                            "/*"
                                        ]
                                    ]
                                }
                            ],
                            "Principal": {
                                "AWS": "*"
                            },
                            "Condition": {
                                "StringEquals": {
                                    "s3:DataAccessPointAccount": {
                                        "Ref": "AWS::AccountId"
                                    }
                                }
                            }
                        }
                    ]
                }
            }
        },
        "VPC": {
            "Type": "AWS::EC2::VPC",
            "Properties": {
                "CidrBlock": "10.0.0.0/16"
            }
        },
        "S3AccessPoint": {
            "Type": "AWS::S3::AccessPoint",
            "Properties": {
                "Bucket": {
                    "Ref": "S3Bucket"
                },
                "Name": "my-access-point",
                "VpcConfiguration": {
                    "VpcId": {
                        "Ref": "VPC"
                    }
                },
                "PublicAccessBlockConfiguration": {
                    "BlockPublicAcls": true,
                    "IgnorePublicAcls": true,
                    "BlockPublicPolicy": true,
                    "RestrictPublicBuckets": true
                }
            }
        }
    },
    "Outputs": {
        "S3AccessPointArn": {
            "Value": {
                "Ref": "S3AccessPoint"
            },
            "Description": "ARN of the sample Amazon S3 access point."
        }
    }
}
```

#### YAML<a name="aws-resource-s3-accesspoint--examples--Create_an_S3_Access_Point_restricted_to_a_VPC--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  S3Bucket:
    Type: AWS::S3::Bucket
  S3BucketPolicy:
    Type: AWS::S3::BucketPolicy
    Properties:
      Bucket:
        Ref: S3Bucket
      PolicyDocument:
        Version: 2012-10-17
        Statement:
          - Action: "*"
            Effect: Allow
            Resource:
              - Fn::GetAtt:
                  - S3Bucket
                  - Arn
              - Fn::Join:
                  - ""
                  - - Fn::GetAtt:
                        - S3Bucket
                        - Arn
                    - /*
            Principal:
              AWS: "*"
            Condition:
              StringEquals:
                s3:DataAccessPointAccount:
                  Ref: AWS::AccountId
  VPC:
    Type: AWS::EC2::VPC
    Properties:
      CidrBlock: 10.0.0.0/16
  S3AccessPoint:
    Type: AWS::S3::AccessPoint
    Properties:
      Bucket:
        Ref: S3Bucket
      Name: my-access-point
      VpcConfiguration:
        VpcId:
          Ref: VPC
      PublicAccessBlockConfiguration:
        BlockPublicAcls: true
        IgnorePublicAcls: true
        BlockPublicPolicy: true
        RestrictPublicBuckets: true
Outputs:
  S3AccessPointArn:
    Value:
      Ref: S3AccessPoint
    Description: ARN of the sample Amazon S3 access point.
```