# AWS::Config::AggregationAuthorization<a name="aws-resource-config-aggregationauthorization"></a>

The `AWS::Config::AggregationAuthorization` resource to grant permission to an aggregator account to collect your AWS Config data\. 

**Topics**
+ [Syntax](#aws-resource-config-aggregationauthorization-syntax)
+ [Properties](#aws-resource-config-aggregationauthorization-properties)
+ [Return Values](#aws-resource-config-aggregationauthorization-returnvalues)
+ [Examples](#aws-resource-config-aggregationauthorization-examples)

## Syntax<a name="aws-resource-config-aggregationauthorization-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-config-aggregationauthorization-syntax.json"></a>

```
{
  "Type" : "AWS::Config::AggregationAuthorization",
  "Properties" : {
    "[AuthorizedAccountId](#cfn-config-aggregationauthorization-authorizedaccountid)" : String,
    "[AuthorizedAwsRegion](#cfn-config-aggregationauthorization-authorizedawsregion)" : String
  }
}
```

### YAML<a name="aws-resource-config-aggregationauthorization-syntax.yaml"></a>

```
Type: "AWS::Config::AggregationAuthorization"
Properties:
  [AuthorizedAccountId](#cfn-config-aggregationauthorization-authorizedaccountid): String
  [AuthorizedAwsRegion](#cfn-config-aggregationauthorization-authorizedawsregion): String
```

## Properties<a name="aws-resource-config-aggregationauthorization-properties"></a>

`AuthorizedAccountId`  <a name="cfn-config-aggregationauthorization-authorizedaccountid"></a>
The 12 digit account ID of the account authorized to aggregate data\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`AuthorizedAwsRegion`  <a name="cfn-config-aggregationauthorization-authorizedawsregion"></a>
The region authorized to collect aggregated data\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-config-aggregationauthorization-returnvalues"></a>

### Ref<a name="aws-resource-config-aggregationauthorization-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the ARN of the AggregationAuthorization, for example:

```
arn:aws:config:us-east-1:123456789012:aggregation-authorization/987654321012/us-west-2
```

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-config-aggregationauthorization-examples"></a>

### AggregationAuthorization<a name="aws-resource-config-aggregationauthorization-example1"></a>

The following example creates an AggregationAuthorization that authorizes another account to aggregate your AWS Config data into a specific region\.

#### JSON<a name="aws-resource-config-aggregationauthorization-example1.json"></a>

```
"AggregationAuthorization": {
    "Type": "AWS::Config::AggregationAuthorization",
    "Properties": {
      "AuthorizedAccountId": 123456789012,
      "AuthorizedAwsRegion": "us-west-2"
    }
  }
```

#### YAML<a name="aws-resource-config-aggregationauthorization-example1.yaml"></a>

```
AggregationAuthorization: 
    Type: "AWS::Config::AggregationAuthorization"
    Properties: 
      AuthorizedAccountId: 123456789012
      AuthorizedAwsRegion: us-west-2
```

### <a name="aws-resource-config-aggregationauthorization-example2"></a>

The following example enables AWS Config, creates an AWS Config rule, an aggregator, and an authorization\.

#### JSON<a name="aws-resource-config-aggregationauthorization-example2.json"></a>

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
                    "default": "Aggregator account"
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
                "Name": "default",
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

#### YAML<a name="aws-resource-config-aggregationauthorization-example2.yaml"></a>

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
        default: Aggregator account
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
    Type: "AWS::Config::ConfigRule"
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
      Name: default
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