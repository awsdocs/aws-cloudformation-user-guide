# AWS::KinesisAnalyticsV2::Application<a name="aws-resource-kinesisanalyticsv2-application"></a>

Creates an Amazon Kinesis Data Analytics application\. For information about creating a Kinesis Data Analytics application, see [Creating an Application](https://docs.aws.amazon.com/kinesisanalytics/latest/java/getting-started.html)\. 

## Syntax<a name="aws-resource-kinesisanalyticsv2-application-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kinesisanalyticsv2-application-syntax.json"></a>

```
{
  "Type" : "AWS::KinesisAnalyticsV2::Application",
  "Properties" : {
      "[ApplicationConfiguration](#cfn-kinesisanalyticsv2-application-applicationconfiguration)" : ApplicationConfiguration,
      "[ApplicationDescription](#cfn-kinesisanalyticsv2-application-applicationdescription)" : String,
      "[ApplicationName](#cfn-kinesisanalyticsv2-application-applicationname)" : String,
      "[RuntimeEnvironment](#cfn-kinesisanalyticsv2-application-runtimeenvironment)" : String,
      "[ServiceExecutionRole](#cfn-kinesisanalyticsv2-application-serviceexecutionrole)" : String,
      "[Tags](#cfn-kinesisanalyticsv2-application-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-kinesisanalyticsv2-application-syntax.yaml"></a>

```
Type: AWS::KinesisAnalyticsV2::Application
Properties: 
  [ApplicationConfiguration](#cfn-kinesisanalyticsv2-application-applicationconfiguration): 
    ApplicationConfiguration
  [ApplicationDescription](#cfn-kinesisanalyticsv2-application-applicationdescription): String
  [ApplicationName](#cfn-kinesisanalyticsv2-application-applicationname): String
  [RuntimeEnvironment](#cfn-kinesisanalyticsv2-application-runtimeenvironment): String
  [ServiceExecutionRole](#cfn-kinesisanalyticsv2-application-serviceexecutionrole): String
  [Tags](#cfn-kinesisanalyticsv2-application-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-kinesisanalyticsv2-application-properties"></a>

`ApplicationConfiguration`  <a name="cfn-kinesisanalyticsv2-application-applicationconfiguration"></a>
Use this parameter to configure the application\.  
*Required*: No  
*Type*: [ApplicationConfiguration](aws-properties-kinesisanalyticsv2-application-applicationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ApplicationDescription`  <a name="cfn-kinesisanalyticsv2-application-applicationdescription"></a>
The description of the application\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ApplicationName`  <a name="cfn-kinesisanalyticsv2-application-applicationname"></a>
The name of the application\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9_.-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RuntimeEnvironment`  <a name="cfn-kinesisanalyticsv2-application-runtimeenvironment"></a>
The runtime environment for the application \(`SQL-1_0`, `FLINK-1_6`, `FLINK-1_8`, or `FLINK-1_11`\)\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `FLINK-1_11 | FLINK-1_6 | FLINK-1_8 | SQL-1_0`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServiceExecutionRole`  <a name="cfn-kinesisanalyticsv2-application-serviceexecutionrole"></a>
Specifies the IAM role that the application uses to access external resources\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `arn:.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-kinesisanalyticsv2-application-tags"></a>
A list of one or more tags to assign to the application\. A tag is a key\-value pair that identifies an application\. Note that the maximum number of application tags includes system tags\. The maximum number of user\-defined application tags is 50\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-resource-kinesisanalyticsv2-application--examples"></a>



### Create an application<a name="aws-resource-kinesisanalyticsv2-application--examples--Create_an_application"></a>

#### JSON<a name="aws-resource-kinesisanalyticsv2-application--examples--Create_an_application--json"></a>

```
{
    "Description": "Sample KinesisAnalytics via CloudFormation",
    "Resources": {
        "BasicApplication": {
            "Type": "AWS::KinesisAnalyticsV2::Application",
            "Properties": {
                "ApplicationName": "sampleApplication",
                "ApplicationDescription": "SampleApp",
                "RuntimeEnvironment": "SQL-1_0",
                "ServiceExecutionRole": {
                    "Fn::GetAtt": [
                        "ServiceExecutionRole",
                        "Arn"
                    ]
                },
                "ApplicationConfiguration": {
                    "SqlApplicationConfiguration": {
                        "Inputs": [
                            {
                                "NamePrefix": "exampleNamePrefix",
                                "InputSchema": {
                                    "RecordColumns": [
                                        {
                                            "Name": "example",
                                            "SqlType": "VARCHAR(16)",
                                            "Mapping": "$.example"
                                        }
                                    ],
                                    "RecordFormat": {
                                        "RecordFormatType": "JSON",
                                        "MappingParameters": {
                                            "JSONMappingParameters": {
                                                "RecordRowPath": "$"
                                            }
                                        }
                                    }
                                },
                                "KinesisStreamsInput": {
                                    "ResourceARN": {
                                        "Fn::GetAtt": [
                                            "InputKinesisStream",
                                            "Arn"
                                        ]
                                    }
                                }
                            }
                        ]
                    },
                    "ApplicationCodeConfiguration": {
                        "CodeContent": {
                            "TextContent": "Example Application Code"
                        },
                        "CodeContentType": "PLAINTEXT"
                    }
                }
            }
        },
        "ServiceExecutionRole": {
            "Type": "AWS::IAM::Role",
            "Properties": {
                "AssumeRolePolicyDocument": {
                    "Version": "2012-10-17",
                    "Statement": [
                        {
                            "Effect": "Allow",
                            "Principal": {
                                "Service": "kinesisanalytics.amazonaws.com"
                            },
                            "Action": "sts:AssumeRole"
                        }
                    ]
                },
                "Path": "/",
                "Policies": [
                    {
                        "PolicyName": "Open",
                        "PolicyDocument": {
                            "Version": "2012-10-17",
                            "Statement": [
                                {
                                    "Effect": "Allow",
                                    "Action": "*",
                                    "Resource": "*"
                                }
                            ]
                        }
                    } 
                ]
            }
        },
        "InputKinesisStream": {
            "Type": "AWS::Kinesis::Stream",
            "Properties": {
                "ShardCount": 1
            }
        },
        "KinesisAnalyticsRole": {
            "Type": "AWS::IAM::Role",
            "Properties": {
                "AssumeRolePolicyDocument": {
                    "Version": "2012-10-17",
                    "Statement": [
                        {
                            "Effect": "Allow",
                            "Principal": {
                                "Service": "kinesisanalytics.amazonaws.com"
                            },
                            "Action": "sts:AssumeRole"
                        }
                    ]
                },
                "Path": "/",
                "Policies": [
                    {
                        "PolicyName": "Open",
                        "PolicyDocument": {
                            "Version": "2012-10-17",
                            "Statement": [
                                {
                                    "Effect": "Allow",
                                    "Action": "*",
                                    "Resource": "*"
                                }
                            ]
                        }
                    }
                ]
            }
        },
        "BasicApplicationOutputs": {
            "Type": "AWS::KinesisAnalyticsV2::ApplicationOutput",
            "DependsOn": "BasicApplication",
            "Properties": {
                "ApplicationName": {
                    "Ref": "BasicApplication"
                },
                "Output": {
                    "Name": "exampleOutput",
                    "DestinationSchema": {
                        "RecordFormatType": "CSV"
                    },
                    "KinesisStreamsOutput": {
                        "ResourceARN": {
                            "Fn::GetAtt": [
                                "OutputKinesisStream",
                                "Arn"
                            ]
                        }
                    }
                }
            }
        },
        "OutputKinesisStream": {
            "Type": "AWS::Kinesis::Stream",
            "Properties": {
                "ShardCount": 1
            }
        },
        "BasicApplicationReferenceDataSource": {
            "Type": "AWS::KinesisAnalyticsV2::ApplicationReferenceDataSource",
            "DependsOn": "BasicApplicationOutputs",
            "Properties": {
                "ApplicationName": {
                    "Ref": "BasicApplication"
                },
                "ReferenceDataSource": {
                    "TableName": "exampleTable",
                    "ReferenceSchema": {
                        "RecordColumns": [
                            {
                                "Name": "example",
                                "SqlType": "VARCHAR(16)",
                                "Mapping": "$.example"
                            }
                        ],
                        "RecordFormat": {
                            "RecordFormatType": "JSON",
                            "MappingParameters": {
                                "JSONMappingParameters": {
                                    "RecordRowPath": "$"
                                }
                            }
                        }
                    },
                    "S3ReferenceDataSource": {
                        "BucketARN": {
                            "Fn::GetAtt": [
                                "S3Bucket",
                                "Arn"
                            ]
                        },
                        "FileKey": "fakeKey"
                    }
                }
            }
        },
        "S3Bucket": {
            "Type": "AWS::S3::Bucket"
        }
    },
    "Outputs": {
        "ApplicationPhysicalResourceId": {
            "Value": {
                "Ref": "BasicApplication"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-kinesisanalyticsv2-application--examples--Create_an_application--yaml"></a>

```
Description: Sample KinesisAnalytics via CloudFormation

Description: Sample KinesisAnalytics via CloudFormation
Resources:
  BasicApplication:
    Type: 'AWS::KinesisAnalyticsV2::Application'
    Properties:
      ApplicationName: sampleApplication
      ApplicationDescription: SampleApp
      RuntimeEnvironment: SQL-1_0
      ServiceExecutionRole: !GetAtt 
        - ServiceExecutionRole
        - Arn
      ApplicationConfiguration:
        SqlApplicationConfiguration:
          Inputs:
            - NamePrefix: exampleNamePrefix
              InputSchema:
                RecordColumns:
                  - Name: example
                    SqlType: VARCHAR(16)
                    Mapping: $.example
                RecordFormat:
                  RecordFormatType: JSON
                  MappingParameters:
                    JSONMappingParameters:
                      RecordRowPath: $
              KinesisStreamsInput:
                ResourceARN: !GetAtt 
                  - InputKinesisStream
                  - Arn
        ApplicationCodeConfiguration:
          CodeContent:
            TextContent: Example Application Code
          CodeContentType: PLAINTEXT
  ServiceExecutionRole:
    Type: 'AWS::IAM::Role'
    Properties:
      AssumeRolePolicyDocument:
        Version: 2012-10-17
        Statement:
          - Effect: Allow
            Principal:
              Service: kinesisanalytics.amazonaws.com
            Action: 'sts:AssumeRole'
      Path: /
      Policies:
        - PolicyName: Open
          PolicyDocument:
            Version: 2012-10-17
            Statement:
              - Effect: Allow
                Action: '*'
                Resource: '*'
  InputKinesisStream:
    Type: 'AWS::Kinesis::Stream'
    Properties:
      ShardCount: 1
  KinesisAnalyticsRole:
    Type: 'AWS::IAM::Role'
    Properties:
      AssumeRolePolicyDocument:
        Version: 2012-10-17
        Statement:
          - Effect: Allow
            Principal:
              Service: kinesisanalytics.amazonaws.com
            Action: 'sts:AssumeRole'
      Path: /
      Policies:
        - PolicyName: Open
          PolicyDocument:
            Version: 2012-10-17
            Statement:
              - Effect: Allow
                Action: '*'
                Resource: '*'
  BasicApplicationOutputs:
    Type: 'AWS::KinesisAnalyticsV2::ApplicationOutput'
    DependsOn: BasicApplication
    Properties:
      ApplicationName: !Ref BasicApplication
      Output:
        Name: exampleOutput
        DestinationSchema:
          RecordFormatType: CSV
        KinesisStreamsOutput:
          ResourceARN: !GetAtt 
            - OutputKinesisStream
            - Arn
  OutputKinesisStream:
    Type: 'AWS::Kinesis::Stream'
    Properties:
      ShardCount: 1
  BasicApplicationReferenceDataSource:
    Type: 'AWS::KinesisAnalyticsV2::ApplicationReferenceDataSource'
    DependsOn: BasicApplicationOutputs
    Properties:
      ApplicationName: !Ref BasicApplication
      ReferenceDataSource:
        TableName: exampleTable
        ReferenceSchema:
          RecordColumns:
            - Name: example
              SqlType: VARCHAR(16)
              Mapping: $.example
          RecordFormat:
            RecordFormatType: JSON
            MappingParameters:
              JSONMappingParameters:
                RecordRowPath: $
        S3ReferenceDataSource:
          BucketARN: !GetAtt 
            - S3Bucket
            - Arn
          FileKey: fakeKey
  S3Bucket:
    Type: 'AWS::S3::Bucket'
Outputs:
  ApplicationPhysicalResourceId:
    Value: !Ref BasicApplication
```

## See also<a name="aws-resource-kinesisanalyticsv2-application--seealso"></a>
+  [CreateApplication](https://docs.aws.amazon.com/kinesisanalytics/latest/apiv2/API_CreateApplication.html) in the *Amazon Kinesis Data Analytics API Reference* 

