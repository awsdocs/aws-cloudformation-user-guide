# AWS::KinesisFirehose::DeliveryStream<a name="aws-resource-kinesisfirehose-deliverystream"></a>

The `AWS::KinesisFirehose::DeliveryStream` resource creates an Amazon Kinesis Firehose \(Kinesis Firehose\) delivery stream that delivers real\-time streaming data to an Amazon Simple Storage Service \(Amazon S3\), Amazon Redshift, or Amazon Elasticsearch Service \(Amazon ES\) destination\. For more information, see [Creating an Amazon Kinesis Firehose Delivery Stream](http://docs.aws.amazon.com/firehose/latest/dev/basic-create.html) in the *Amazon Kinesis Firehose Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-kinesisfirehose-deliverystream-syntax)
+ [Properties](#aws-resource-kinesisfirehose-deliverystream-properties)
+ [Return Values](#aws-resource-kinesisfirehose-deliverystream-returnvalues)
+ [Examples](#aws-resource-kinesisfirehose-deliverystream-examples)
+ [See Also](#aws-resource-kinesisfirehose-deliverystream-seealso)

## Syntax<a name="aws-resource-kinesisfirehose-deliverystream-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kinesisfirehose-deliverystream-syntax.json"></a>

```
{
  "Type" : "AWS::KinesisFirehose::DeliveryStream",
  "Properties" : {
    "[DeliveryStreamName](#cfn-kinesisfirehose-deliverystream-deliverystreamname)" : String,
    "[DeliveryStreamType](#cfn-kinesisfirehose-deliverystream-deliverystreamtype)" : String,
    "[ElasticsearchDestinationConfiguration](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration)" : [*ElasticsearchDestinationConfiguration*](aws-properties-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration.md),
    "[ExtendedS3DestinationConfiguration](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration)" : [*ExtendedS3DestinationConfiguration*](aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration.md),
    "[KinesisStreamSourceConfiguration](#cfn-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration)" : [*KinesisStreamSourceConfiguration*](aws-properties-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration.md),
    "[RedshiftDestinationConfiguration](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration)" : [*RedshiftDestinationConfiguration*](aws-properties-kinesisfirehose-deliverystream-redshiftdestinationconfiguration.md),
    "[S3DestinationConfiguration](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration)" : [*S3DestinationConfiguration*](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md),
    "[SplunkDestinationConfiguration](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration)" : [*SplunkDestinationConfiguration*](aws-properties-kinesisfirehose-deliverystream-splunkdestinationconfiguration.md)
  }
}
```

### YAML<a name="aws-resource-kinesisfirehose-deliverystream-syntax.yaml"></a>

```
Type: "AWS::KinesisFirehose::DeliveryStream"
Properties: 
  [DeliveryStreamName](#cfn-kinesisfirehose-deliverystream-deliverystreamname): String
  [DeliveryStreamType](#cfn-kinesisfirehose-deliverystream-deliverystreamtype): String
  [ElasticsearchDestinationConfiguration](#cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration):
    [*ElasticsearchDestinationConfiguration*](aws-properties-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration.md)
  [ExtendedS3DestinationConfiguration](#cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration):
    [*ExtendedS3DestinationConfiguration*](aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration.md)
  [KinesisStreamSourceConfiguration](#cfn-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration):
    [*KinesisStreamSourceConfiguration*](aws-properties-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration.md)
  [RedshiftDestinationConfiguration](#cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration):
    [*RedshiftDestinationConfiguration*](aws-properties-kinesisfirehose-deliverystream-redshiftdestinationconfiguration.md)
  [S3DestinationConfiguration](#cfn-kinesisfirehose-deliverystream-s3destinationconfiguration):
    [*S3DestinationConfiguration*](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md)
  [SplunkDestinationConfiguration](#cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration):
    [*SplunkDestinationConfiguration*](aws-properties-kinesisfirehose-deliverystream-splunkdestinationconfiguration.md)
```

## Properties<a name="aws-resource-kinesisfirehose-deliverystream-properties"></a>

`DeliveryStreamName`  <a name="cfn-kinesisfirehose-deliverystream-deliverystreamname"></a>
A name for the delivery stream\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DeliveryStreamType`  <a name="cfn-kinesisfirehose-deliverystream-deliverystreamtype"></a>
The delivery stream type\. This property can be one of the following values:  
+ `DirectPut`: Provider applications access the delivery stream directly\.
+ `KinesisStreamAsSource`: The delivery stream uses a Kinesis stream as a source\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ElasticsearchDestinationConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration"></a>
An Amazon ES destination for the delivery stream\.  
*Required*: Conditional\. You must specify only one destination configuration\.  
*Type*: [Kinesis Firehose DeliveryStream ElasticsearchDestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-elasticsearchdestinationconfiguration.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\. If you change the delivery stream destination from an Amazon ES destination to an Amazon S3 or Amazon Redshift destination, update requires [some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)\.

`ExtendedS3DestinationConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-extendeds3destinationconfiguration"></a>
An Amazon S3 destination for the delivery stream\.  
*Required*: Conditional\. You must specify only one destination configuration\.  
 *Type*: [Kinesis Firehose DeliveryStream ExtendedS3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\. If you change the delivery stream destination from an Amazon Redshift destination to an Amazon ES destination, update requires [some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)\.

`KinesisStreamSourceConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration"></a>
When a Kinesis stream is used as the source for the delivery stream, a [Kinesis Data Firehose DeliveryStream KinesisStreamSourceConfiguration](aws-properties-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration.md) containing the Kinesis stream ARN and the role ARN for the source stream\.  
*Required*: No  
*Type*: [Kinesis Data Firehose DeliveryStream KinesisStreamSourceConfiguration](aws-properties-kinesisfirehose-deliverystream-kinesisstreamsourceconfiguration.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RedshiftDestinationConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-redshiftdestinationconfiguration"></a>
An Amazon Redshift destination for the delivery stream\.  
*Required*: Conditional\. You must specify only one destination configuration\.  
*Type*: [Kinesis Firehose DeliveryStream RedshiftDestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-redshiftdestinationconfiguration.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\. If you change the delivery stream destination from an Amazon Redshift destination to an Amazon ES destination, update requires [some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)\.

`S3DestinationConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-s3destinationconfiguration"></a>
An Amazon S3 destination for the delivery stream\.  
*Required*: Conditional\. You must specify only one destination configuration\.  
*Type*: [Kinesis Firehose DeliveryStream S3DestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\. If you change the delivery stream destination from an Amazon S3 destination to an Amazon ES destination, update requires [some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)\.

`SplunkDestinationConfiguration`  <a name="cfn-kinesisfirehose-deliverystream-splunkdestinationconfiguration"></a>
The configuration of a destination in Splunk for the delivery stream\.  
*Required*: No  
*Type*: [Kinesis Data Firehose DeliveryStream SplunkDestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-splunkdestinationconfiguration.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="aws-resource-kinesisfirehose-deliverystream-returnvalues"></a>

### Ref<a name="aws-resource-kinesisfirehose-deliverystream-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the delivery stream name, such as `mystack-deliverystream-1ABCD2EF3GHIJ`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-resource-kinesisfirehose-deliverystream-getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Arn`  
The Amazon Resource Name \(ARN\) of the delivery stream, such as `arn:aws:firehose:``us-east-2``:123456789012:deliverystream/delivery-stream-name`\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="aws-resource-kinesisfirehose-deliverystream-examples"></a>

### <a name="aws-resource-kinesisfirehose-deliverystream-example1"></a>

The following example creates a Kinesis Firehose delivery stream that delivers data to an Amazon ES destination\. Kinesis Firehose backs up all data sent to the destination in an Amazon S3 bucket\.

#### JSON<a name="aws-resource-kinesisfirehose-deliverystream-example.json"></a>

```
"ElasticSearchDeliveryStream": {
  "Type": "AWS::KinesisFirehose::DeliveryStream",
  "Properties": {
    "ElasticsearchDestinationConfiguration": {
      "BufferingHints": {
        "IntervalInSeconds": 60,
        "SizeInMBs": 50
      },
      "CloudWatchLoggingOptions": {
        "Enabled": true,
        "LogGroupName": "deliverystream",
        "LogStreamName": "elasticsearchDelivery"
      },
      "DomainARN": { "Ref" : "MyDomainARN" },
      "IndexName": { "Ref" : "MyIndexName" },
      "IndexRotationPeriod": "NoRotation",
      "TypeName" : "fromFirehose",
      "RetryOptions": {
         "DurationInSeconds": "60"
      },
      "RoleARN": { "Fn::GetAtt" : ["ESdeliveryRole", "Arn"] },
      "S3BackupMode": "AllDocuments",
      "S3Configuration": { 
        "BucketARN": { "Ref" : "MyBackupBucketARN" },
        "BufferingHints": {
            "IntervalInSeconds": "60",
             "SizeInMBs": "50"
        },
        "CompressionFormat": "UNCOMPRESSED",
        "Prefix": "firehose/",
        "RoleARN": { "Fn::GetAtt" : ["S3deliveryRole", "Arn"] },
        "CloudWatchLoggingOptions" : {
          "Enabled" : true,
          "LogGroupName" : "deliverystream",
          "LogStreamName" : "s3Backup"
        }
      }
    }              
  }
}
```

#### YAML<a name="aws-resource-kinesisfirehose-deliverystream-example.yaml"></a>

```
ElasticSearchDeliveryStream: 
  Type: "AWS::KinesisFirehose::DeliveryStream"
  Properties: 
    ElasticsearchDestinationConfiguration: 
      BufferingHints: 
        IntervalInSeconds: 60
        SizeInMBs: 50
      CloudWatchLoggingOptions: 
        Enabled: true
        LogGroupName: "deliverystream"
        LogStreamName: "elasticsearchDelivery"
      DomainARN: 
        Ref: "MyDomainARN"
      IndexName: 
        Ref: "MyIndexName"
      IndexRotationPeriod: "NoRotation"
      TypeName: "fromFirehose"
      RetryOptions: 
        DurationInSeconds: "60"
      RoleARN: 
        Fn::GetAtt: 
          - "ESdeliveryRole"
          - "Arn"
      S3BackupMode: "AllDocuments"
      S3Configuration: 
        BucketARN: 
          Ref: "MyBackupBucketARN"
        BufferingHints: 
          IntervalInSeconds: "60"
          SizeInMBs: "50"
        CompressionFormat: "UNCOMPRESSED"
        Prefix: "firehose/"
        RoleARN: 
          Fn::GetAtt: 
            - "S3deliveryRole"
            - "Arn"
        CloudWatchLoggingOptions: 
          Enabled: true
          LogGroupName: "deliverystream"
          LogStreamName: "s3Backup"
```

### <a name="aws-resource-kinesisfirehose-deliverystream-example2"></a>

The following example uses the `ExtendedS3DestinationConfiguration` property to specify an Amazon S3 destination for the delivery stream\.

#### JSON<a name="aws-resource-kinesisfirehose-deliverystream-example2.json"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",
  "Description" : "Stack for Firehose DeliveryStream S3 Destination.",
  "Resources": {
    "deliverystream": {
      "DependsOn": ["deliveryPolicy"],
      "Type": "AWS::KinesisFirehose::DeliveryStream",
      "Properties": {
        "ExtendedS3DestinationConfiguration": {
          "BucketARN": {"Fn::Join": ["", ["arn:aws:s3:::", {"Ref":"s3bucket"}]]},
          "BufferingHints": {
            "IntervalInSeconds": "60",
            "SizeInMBs": "50"
          },
          "CompressionFormat": "UNCOMPRESSED",
          "Prefix": "firehose/",
          "RoleARN": {"Fn::GetAtt" : ["deliveryRole", "Arn"] },
          "ProcessingConfiguration" : {
            "Enabled": "true",
            "Processors": [
            {
              "Parameters": [ 
              { 
                "ParameterName": "LambdaArn",
                "ParameterValue": {"Fn::GetAtt" : ["myLambda", "Arn"] } 
              }],
              "Type": "Lambda"
            }]
          }
        }
      }
    },
    "s3bucket": {
      "Type": "AWS::S3::Bucket",
      "Properties": {
        "VersioningConfiguration": {
          "Status": "Enabled"
        }
      }
    },
    "deliveryRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "AssumeRolePolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Sid": "",
              "Effect": "Allow",
              "Principal": {
                "Service": "firehose.amazonaws.com"
              },
              "Action": "sts:AssumeRole",
              "Condition": {
                "StringEquals": {
                  "sts:ExternalId": {"Ref":"AWS::AccountId"}
                }
              }
            }
          ]
        }
      }
    },
    "deliveryPolicy": {
      "Type": "AWS::IAM::Policy",
      "Properties": {
        "PolicyName": "firehose_delivery_policy",
        "PolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Effect": "Allow",
              "Action": [
                "s3:AbortMultipartUpload",
                "s3:GetBucketLocation",
                "s3:GetObject",
                "s3:ListBucket",
                "s3:ListBucketMultipartUploads",
                "s3:PutObject"
              ],
              "Resource": [
                {"Fn::Join": ["", ["arn:aws:s3:::", {"Ref":"s3bucket"}]]},
                {"Fn::Join": ["", ["arn:aws:s3:::", {"Ref":"s3bucket"}, "*"]]}
              ]
            }
          ]
        },
        "Roles": [{"Ref": "deliveryRole"}]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-kinesisfirehose-deliverystream-example2.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Stack for Firehose DeliveryStream S3 Destination.
Resources:
  deliverystream:
    DependsOn:
      - deliveryPolicy
    Type: 'AWS::KinesisFirehose::DeliveryStream'
    Properties:
      ExtendedS3DestinationConfiguration:
        BucketARN: !Join 
          - ''
          - - 'arn:aws:s3:::'
            - !Ref s3bucket
        BufferingHints:
          IntervalInSeconds: '60'
          SizeInMBs: '50'
        CompressionFormat: UNCOMPRESSED
        Prefix: firehose/
        RoleARN: !GetAtt deliveryRole.Arn
        ProcessingConfiguration:
          Enabled: 'true'
          Processors:
            - Parameters:
                - ParameterName: LambdaArn
                  ParameterValue: !GetAtt myLambda.Arn 
              Type: Lambda 
  s3bucket:
    Type: 'AWS::S3::Bucket'
    Properties:
      VersioningConfiguration:
        Status: Enabled
  deliveryRole:
    Type: 'AWS::IAM::Role'
    Properties:
      AssumeRolePolicyDocument:
        Version: 2012-10-17
        Statement:
          - Sid: ''
            Effect: Allow
            Principal:
              Service: firehose.amazonaws.com
            Action: 'sts:AssumeRole'
            Condition:
              StringEquals:
                'sts:ExternalId': !Ref 'AWS::AccountId'
  deliveryPolicy:
    Type: 'AWS::IAM::Policy'
    Properties:
      PolicyName: firehose_delivery_policy
      PolicyDocument:
        Version: 2012-10-17
        Statement:
          - Effect: Allow
            Action:
              - 's3:AbortMultipartUpload'
              - 's3:GetBucketLocation'
              - 's3:GetObject'
              - 's3:ListBucket'
              - 's3:ListBucketMultipartUploads'
              - 's3:PutObject'
            Resource:
              - !Join 
                - ''
                - - 'arn:aws:s3:::'
                  - !Ref s3bucket
              - !Join 
                - ''
                - - 'arn:aws:s3:::'
                  - !Ref s3bucket
                  - '*'
      Roles:
        - !Ref deliveryRole
```

### <a name="aws-resource-kinesisfirehose-deliverystream-example3"></a>

The following example uses the `KinesisStreamSourceConfiguration` property to specify a Kinesis stream as the source for the delivery stream\.

#### JSON<a name="aws-resource-kinesisfirehose-deliverystream-example3.json"></a>

```
{
    "Parameters": {
        "deliveryRoleArn": {
            "Type": "String"
        },
        "deliveryStreamName": {
            "Type": "String"
        },
        "kinesisStreamARN": {
            "Type": "String"
        },
        "kinesisStreamRoleArn": {
            "Type": "String"
        },
        "s3bucketArn": {
            "Type": "String"
        }
    },
    "Resources": {
        "Deliverystream": {
            "Type": "AWS::KinesisFirehose::DeliveryStream",
            "Properties": {
                "DeliveryStreamName": {
                    "Ref": "deliveryStreamName"
                },
                "DeliveryStreamType": "KinesisStreamAsSource",
                "KinesisStreamSourceConfiguration": {
                    "KinesisStreamARN": {
                        "Ref": "kinesisStreamARN"
                    },
                    "RoleARN": {
                        "Ref": "kinesisStreamRoleArn"
                    }
                },
                "ExtendedS3DestinationConfiguration": {
                    "BucketARN": {
                        "Ref": "s3bucketArn"
                    },
                    "BufferingHints": {
                        "IntervalInSeconds": 60,
                        "SizeInMBs": 50,
                        "CompressionFormat": "UNCOMPRESSED"
                    },
                    "Prefix": "firehose/",
                    "RoleARN": {
                        "Ref": "deliveryRoleArn"
                    }
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-kinesisfirehose-deliverystream-example3.yaml"></a>

```
Parameters:
    deliveryRoleArn:
        Type: String
    deliveryStreamName:
        Type: String
    kinesisStreamARN :
        Type : String
    kinesisStreamRoleArn:
        Type : String
    s3bucketArn:
        Type: String
Resources :
    Deliverystream: 
        Type: AWS::KinesisFirehose::DeliveryStream
        Properties: 
            DeliveryStreamName: !Ref deliveryStreamName
            DeliveryStreamType: KinesisStreamAsSource
            KinesisStreamSourceConfiguration: 
                KinesisStreamARN: !Ref kinesisStreamARN
                RoleARN: !Ref kinesisStreamRoleArn
            ExtendedS3DestinationConfiguration: 
                BucketARN: !Ref s3bucketArn
                BufferingHints: 
                    IntervalInSeconds: 60
                    SizeInMBs: 50
                    CompressionFormat: UNCOMPRESSED
                Prefix: firehose/
                RoleARN: !Ref deliveryRoleArn
```

## See Also<a name="aws-resource-kinesisfirehose-deliverystream-seealso"></a>
+ [ CreateDeliveryStream](http://docs.aws.amazon.com/firehose/latest/APIReference/API_CreateDeliveryStream.html) in the *Amazon Kinesis Firehose API Reference*