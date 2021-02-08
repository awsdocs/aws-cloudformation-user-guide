# AWS::Config::AggregationAuthorization<a name="aws-resource-config-aggregationauthorization"></a>

An object that represents the authorizations granted to aggregator accounts and regions\.

## Syntax<a name="aws-resource-config-aggregationauthorization-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-config-aggregationauthorization-syntax.json"></a>

```
{
  "Type" : "AWS::Config::AggregationAuthorization",
  "Properties" : {
      "[AuthorizedAccountId](#cfn-config-aggregationauthorization-authorizedaccountid)" : String,
      "[AuthorizedAwsRegion](#cfn-config-aggregationauthorization-authorizedawsregion)" : String,
      "[Tags](#cfn-config-aggregationauthorization-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-config-aggregationauthorization-syntax.yaml"></a>

```
Type: AWS::Config::AggregationAuthorization
Properties: 
  [AuthorizedAccountId](#cfn-config-aggregationauthorization-authorizedaccountid): String
  [AuthorizedAwsRegion](#cfn-config-aggregationauthorization-authorizedawsregion): String
  [Tags](#cfn-config-aggregationauthorization-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-config-aggregationauthorization-properties"></a>

`AuthorizedAccountId`  <a name="cfn-config-aggregationauthorization-authorizedaccountid"></a>
The 12\-digit account ID of the account authorized to aggregate data\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `\d{12}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AuthorizedAwsRegion`  <a name="cfn-config-aggregationauthorization-authorizedawsregion"></a>
The region authorized to collect aggregated data\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-config-aggregationauthorization-tags"></a>
An array of tag object\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-config-aggregationauthorization-return-values"></a>

### Ref<a name="aws-resource-config-aggregationauthorization-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the AggregationAuthorization, such as `arn:aws:config:us-east-1:123456789012:aggregation-authorization/987654321012/us-west-2`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-config-aggregationauthorization--examples"></a>



### Authorize Another Account<a name="aws-resource-config-aggregationauthorization--examples--Authorize_Another_Account"></a>

The following example creates an AggregationAuthorization that authorizes another account to aggregate your AWS Config data into a specific region\. 

#### JSON<a name="aws-resource-config-aggregationauthorization--examples--Authorize_Another_Account--json"></a>

```
"AggregationAuthorization": {
    "Type": "AWS::Config::AggregationAuthorization",
    "Properties": {
        "AuthorizedAccountId": 123456789012,
        "AuthorizedAwsRegion": "us-west-2"
    }
}
```

#### YAML<a name="aws-resource-config-aggregationauthorization--examples--Authorize_Another_Account--yaml"></a>

```
AggregationAuthorization: 
  Type: "AWS::Config::AggregationAuthorization"
  Properties: 
    AuthorizedAccountId: 123456789012
    AuthorizedAwsRegion: us-west-2
```

### Aggregation Authorization<a name="aws-resource-config-aggregationauthorization--examples--Aggregation_Authorization"></a>

The following example enables AWS Config and creates an AWS Config rule, an aggregator, and an authorization\.

#### JSON<a name="aws-resource-config-aggregationauthorization--examples--Aggregation_Authorization--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "Enable AWS Config",
    "Metadata": {
        "AWS::CloudFormation::Interface": {
            "ParameterGroups": [
                {
                    "Label": {
                        "default": "Configuration Recorder Configuration"
                    },
                    "Parameters": [
                        "GlobalResourceTypesRegion"
                    ]
                },
                {
                    "Label": {
                        "default": "Configuration Aggregator Configuration"
                    },
                    "Parameters": [
                        "AggregatorAccount",
                        "AggregatorRegion",
                        "SourceAccounts",
                        "SourceRegions"
                    ]
                }
            ],
            "ParameterLabels": {
                "GlobalResourceTypesRegion": {
                    "default": "Global resource types region"
                },
                "AggregatorAccount": {
                    "default": "Aggregator account"
                },
                "AggregatorRegion": {
                    "default": "Aggregator region"
                },
                "SourceAccounts": {
                    "default": "Source accounts"
                },
                "SourceRegions": {
                    "default": "Source regions"
                }
            }
        }
    },
    "Parameters": {
        "GlobalResourceTypesRegion": {
            "Type": "String",
            "Default": "us-east-1",
            "Description": "AWS region used to record global resources types"
        },
        "AggregatorAccount": {
            "Type": "String",
            "Description": "Account ID of the aggregator"
        },
        "AggregatorRegion": {
            "Type": "String",
            "Default": "us-east-1",
            "Description": "AWS region of the aggregator"
        },
        "SourceAccounts": {
            "Type": "CommaDelimitedList",
            "Description": "List of source accounts to aggregate"
        },
        "SourceRegions": {
            "Type": "CommaDelimitedList",
            "Description": "List of regions to aggregate"
        }
    },
    "Conditions": {
        "IncludeGlobalResourceTypes": {
            "Fn::Equals": [
                {
                    "Ref": "GlobalResourceTypesRegion"
                },
                {
                    "Ref": "AWS::Region"
                }
            ]
        },
        "CreateAggregator": {
            "Fn::And": [
                {
                    "Fn::Equals": [
                        {
                            "Ref": "AggregatorAccount"
                        },
                        {
                            "Ref": "AWS::AccountId"
                        }
                    ]
                },
                {
                    "Fn::Equals": [
                        {
                            "Ref": "AggregatorRegion"
                        },
                        {
                            "Ref": "AWS::Region"
                        }
                    ]
                }
            ]
        },
        "CreateAuthorization": {
            "Fn::Not": [
                {
                    "Fn::Equals": [
                        {
                            "Ref": "AggregatorAccount"
                        },
                        {
                            "Ref": "AWS::AccountId"
                        }
                    ]
                }
            ]
        }
    },
    "Resources": {
        "ConfigBucket": {
            "DeletionPolicy": "Retain",
            "Type": "AWS::S3::Bucket"
        },
        "ConfigBucketPolicy": {
            "Type": "AWS::S3::BucketPolicy",
            "Properties": {
                "Bucket": {
                    "Ref": "ConfigBucket"
                },
                "PolicyDocument": {
                    "Version": "2012-10-17",
                    "Statement": [
                        {
                            "Sid": "AWSConfigBucketPermissionsCheck",
                            "Effect": "Allow",
                            "Principal": {
                                "Service": [
                                    "config.amazonaws.com"
                                ]
                            },
                            "Action": "s3:GetBucketAcl",
                            "Resource": [
                                {
                                    "Fn::Sub": "arn:aws:s3:::${ConfigBucket}"
                                }
                            ]
                        },
                        {
                            "Sid": "AWSConfigBucketDelivery",
                            "Effect": "Allow",
                            "Principal": {
                                "Service": [
                                    "config.amazonaws.com"
                                ]
                            },
                            "Action": "s3:PutObject",
                            "Resource": [
                                {
                                    "Fn::Sub": "arn:aws:s3:::${ConfigBucket}/AWSLogs/${AWS::AccountId}/*"
                                }
                            ]
                        }
                    ]
                }
            }
        },
        "ConfigRecorderRole": {
            "Type": "AWS::IAM::Role",
            "Properties": {
                "AssumeRolePolicyDocument": {
                    "Version": "2012-10-17",
                    "Statement": [
                        {
                            "Effect": "Allow",
                            "Principal": {
                                "Service": [
                                    "config.amazonaws.com"
                                ]
                            },
                            "Action": [
                                "sts:AssumeRole"
                            ]
                        }
                    ]
                },
                "Path": "/",
                "ManagedPolicyArns": [
                    "arn:aws:iam::aws:policy/service-role/AWSConfigRole"
                ]
            }
        },
        "ConfigRecorder": {
            "Type": "AWS::Config::ConfigurationRecorder",
            "DependsOn": [
                "ConfigRecorderRole",
                "ConfigBucketPolicy"
            ],
            "Properties": {
                "RoleARN": {
                    "Fn::GetAtt": [
                        "ConfigRecorderRole",
                        "Arn"
                    ]
                },
                "RecordingGroup": {
                    "AllSupported": true,
                    "IncludeGlobalResourceTypes": {
                        "Fn::If": [
                            "IncludeGlobalResourceTypes",
                            true,
                            false
                        ]
                    }
                }
            }
        },
        "DeliveryChannel": {
            "Type": "AWS::Config::DeliveryChannel",
            "DependsOn": [
                "ConfigBucketPolicy"
            ],
            "Properties": {
                "Name": "default",
                "S3BucketName": {
                    "Ref": "ConfigBucket"
                }
            }
        },
        "S3BucketPublicReadRule": {
            "Type": "AWS::Config::ConfigRule",
            "DependsOn": [
                "ConfigRecorder"
            ],
            "Properties": {
                "ConfigRuleName": "stackset-s3-bucket-public-read-prohibited",
                "Description": "s3-bucket-public-read-prohibited from stackset",
                "Scope": {
                    "ComplianceResourceTypes": [
                        "AWS::S3::Bucket"
                    ]
                },
                "Source": {
                    "Owner": "AWS",
                    "SourceIdentifier": "S3_BUCKET_PUBLIC_READ_PROHIBITED"
                }
            }
        },
        "ConfigAggregator": {
            "Type": "AWS::Config::ConfigurationAggregator",
            "Condition": "CreateAggregator",
            "Properties": {
                "Name": "name",
                "AccountAggregationSources": [
                    {
                        "AccountIds": {
                            "Ref": "SourceAccounts"
                        },
                        "AwsRegions": {
                            "Ref": "SourceRegions"
                        }
                    }
                ]
            }
        },
        "AggregationAuthorization": {
            "Type": "AWS::Config::AggregationAuthorization",
            "Condition": "CreateAuthorization",
            "Properties": {
                "AuthorizedAccountId": {
                    "Ref": "AggregatorAccount"
                },
                "AuthorizedAwsRegion": {
                    "Ref": "AggregatorRegion"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-config-aggregationauthorization--examples--Aggregation_Authorization--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Enable AWS Config

Metadata:
  AWS::CloudFormation::Interface:
    ParameterGroups:
      - Label:
          default: Configuration Recorder Configuration
        Parameters:
          - GlobalResourceTypesRegion
      - Label:
          default: Configuration Aggregator Configuration
        Parameters:
          - AggregatorAccount
          - AggregatorRegion
          - SourceAccounts
          - SourceRegions
    ParameterLabels:
      GlobalResourceTypesRegion:
        default: Global resource types region
      AggregatorAccount:
        default: Aggregator account
      AggregatorRegion:
        default: Aggregator region
      SourceAccounts:
        default: Source accounts
      SourceRegions:
        default: Source regions

Parameters:
  GlobalResourceTypesRegion:
    Type: String
    Default: us-east-1
    Description: AWS region used to record global resources types
  AggregatorAccount:
    Type: String
    Description: Account ID of the aggregator
  AggregatorRegion:
    Type: String
    Default: us-east-1
    Description: AWS region of the aggregator
  SourceAccounts:
    Type: CommaDelimitedList
    Description: List of source accounts to aggregate
  SourceRegions:
    Type: CommaDelimitedList
    Description: List of regions to aggregate

Conditions:
  IncludeGlobalResourceTypes: !Equals
    - !Ref GlobalResourceTypesRegion
    - !Ref AWS::Region
  CreateAggregator: !And
    - !Equals
      - !Ref AggregatorAccount
      - !Ref AWS::AccountId
    - !Equals
      - !Ref AggregatorRegion
      - !Ref AWS::Region
  CreateAuthorization: !Not
    - !Equals
      - !Ref AggregatorAccount
      - !Ref AWS::AccountId

Resources:

  ConfigBucket:
    DeletionPolicy: Retain
    Type: AWS::S3::Bucket

  ConfigBucketPolicy:
    Type: AWS::S3::BucketPolicy
    Properties:
      Bucket: !Ref ConfigBucket
      PolicyDocument:
        Version: 2012-10-17
        Statement:
          - Sid: AWSConfigBucketPermissionsCheck
            Effect: Allow
            Principal:
              Service:
                - config.amazonaws.com
            Action: s3:GetBucketAcl
            Resource:
              - !Sub "arn:aws:s3:::${ConfigBucket}"
          - Sid: AWSConfigBucketDelivery
            Effect: Allow
            Principal:
              Service:
                - config.amazonaws.com
            Action: s3:PutObject
            Resource:
              - !Sub "arn:aws:s3:::${ConfigBucket}/AWSLogs/${AWS::AccountId}/*"

  ConfigRecorderRole:
    Type: AWS::IAM::Role
    Properties:
      AssumeRolePolicyDocument:
        Version: 2012-10-17
        Statement:
          - Effect: Allow
            Principal:
              Service:
                - config.amazonaws.com
            Action:
              - sts:AssumeRole
      Path: /
      ManagedPolicyArns:
        - arn:aws:iam::aws:policy/service-role/AWSConfigRole

  ConfigRecorder:
    Type: AWS::Config::ConfigurationRecorder
    DependsOn:
      - ConfigRecorderRole
      - ConfigBucketPolicy
    Properties:
      RoleARN: !GetAtt ConfigRecorderRole.Arn
      RecordingGroup:
        AllSupported: True
        IncludeGlobalResourceTypes: !If
          - IncludeGlobalResourceTypes
          - True
          - False

  DeliveryChannel:
    Type: AWS::Config::DeliveryChannel
    DependsOn:
      - ConfigBucketPolicy
    Properties:
      Name: default
      S3BucketName: !Ref ConfigBucket

  S3BucketPublicReadRule:
    Type: AWS::Config::ConfigRule
    DependsOn:
      - ConfigRecorder
    Properties:
      ConfigRuleName: stackset-s3-bucket-public-read-prohibited
      Description: s3-bucket-public-read-prohibited from stackset
      Scope:
        ComplianceResourceTypes:
          - AWS::S3::Bucket
      Source:
        Owner: AWS
        SourceIdentifier: S3_BUCKET_PUBLIC_READ_PROHIBITED

  ConfigAggregator:
    Type: AWS::Config::ConfigurationAggregator
    Condition: CreateAggregator
    Properties:
    ConfigurationAggregatorName: name
      AccountAggregationSources:
        - AccountIds: !Ref SourceAccounts
          AwsRegions: !Ref SourceRegions

  AggregationAuthorization:
    Type: AWS::Config::AggregationAuthorization
    Condition: CreateAuthorization
    Properties:
      AuthorizedAccountId: !Ref AggregatorAccount
      AuthorizedAwsRegion: !Ref AggregatorRegion
```