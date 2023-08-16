# AWS::S3::Bucket ReplicationRule<a name="aws-properties-s3-bucket-replicationconfiguration-rules"></a>

Specifies which Amazon S3 objects to replicate and where to store the replicas\.

## Syntax<a name="aws-properties-s3-bucket-replicationconfiguration-rules-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-replicationconfiguration-rules-syntax.json"></a>

```
{
  "[DeleteMarkerReplication](#cfn-s3-bucket-replicationrule-deletemarkerreplication)" : DeleteMarkerReplication,
  "[Destination](#cfn-s3-bucket-replicationconfiguration-rules-destination)" : ReplicationDestination,
  "[Filter](#cfn-s3-bucket-replicationrule-filter)" : ReplicationRuleFilter,
  "[Id](#cfn-s3-bucket-replicationconfiguration-rules-id)" : String,
  "[Prefix](#cfn-s3-bucket-replicationconfiguration-rules-prefix)" : String,
  "[Priority](#cfn-s3-bucket-replicationrule-priority)" : Integer,
  "[SourceSelectionCriteria](#cfn-s3-bucket-replicationrule-sourceselectioncriteria)" : SourceSelectionCriteria,
  "[Status](#cfn-s3-bucket-replicationconfiguration-rules-status)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-replicationconfiguration-rules-syntax.yaml"></a>

```
  [DeleteMarkerReplication](#cfn-s3-bucket-replicationrule-deletemarkerreplication): 
    DeleteMarkerReplication
  [Destination](#cfn-s3-bucket-replicationconfiguration-rules-destination): 
    ReplicationDestination
  [Filter](#cfn-s3-bucket-replicationrule-filter): 
    ReplicationRuleFilter
  [Id](#cfn-s3-bucket-replicationconfiguration-rules-id): String
  [Prefix](#cfn-s3-bucket-replicationconfiguration-rules-prefix): String
  [Priority](#cfn-s3-bucket-replicationrule-priority): Integer
  [SourceSelectionCriteria](#cfn-s3-bucket-replicationrule-sourceselectioncriteria): 
    SourceSelectionCriteria
  [Status](#cfn-s3-bucket-replicationconfiguration-rules-status): String
```

## Properties<a name="aws-properties-s3-bucket-replicationconfiguration-rules-properties"></a>

`DeleteMarkerReplication`  <a name="cfn-s3-bucket-replicationrule-deletemarkerreplication"></a>
Specifies whether Amazon S3 replicates delete markers\. If you specify a `Filter` in your replication configuration, you must also include a `DeleteMarkerReplication` element\. If your `Filter` includes a `Tag` element, the `DeleteMarkerReplication` `Status` must be set to Disabled, because Amazon S3 does not support replicating delete markers for tag\-based rules\. For an example configuration, see [Basic Rule Configuration](https://docs.aws.amazon.com/AmazonS3/latest/dev/replication-add-config.html#replication-config-min-rule-config)\.   
For more information about delete marker replication, see [Basic Rule Configuration](https://docs.aws.amazon.com/AmazonS3/latest/dev/delete-marker-replication.html)\.   
If you are using an earlier version of the replication configuration, Amazon S3 handles replication of delete markers differently\. For more information, see [Backward Compatibility](https://docs.aws.amazon.com/AmazonS3/latest/dev/replication-add-config.html#replication-backward-compat-considerations)\.
*Required*: No  
*Type*: [DeleteMarkerReplication](aws-properties-s3-bucket-deletemarkerreplication.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Destination`  <a name="cfn-s3-bucket-replicationconfiguration-rules-destination"></a>
A container for information about the replication destination and its configurations including enabling the S3 Replication Time Control \(S3 RTC\)\.  
*Required*: Yes  
*Type*: [ReplicationDestination](aws-properties-s3-bucket-replicationconfiguration-rules-destination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Filter`  <a name="cfn-s3-bucket-replicationrule-filter"></a>
A filter that identifies the subset of objects to which the replication rule applies\. A `Filter` must specify exactly one `Prefix`, `TagFilter`, or an `And` child element\. The use of the filter field indicates that this is a V2 replication configuration\. This field isn't supported in a V1 replication configuration\.  
V1 replication configuration only supports filtering by key prefix\. To filter using a V1 replication configuration, add the `Prefix` directly as a child element of the `Rule` element\.
*Required*: No  
*Type*: [ReplicationRuleFilter](aws-properties-s3-bucket-replicationrulefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-s3-bucket-replicationconfiguration-rules-id"></a>
A unique identifier for the rule\. The maximum value is 255 characters\. If you don't specify a value, AWS CloudFormation generates a random ID\. When using a V2 replication configuration this property is capitalized as "ID"\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-s3-bucket-replicationconfiguration-rules-prefix"></a>
An object key name prefix that identifies the object or objects to which the rule applies\. The maximum prefix length is 1,024 characters\. To include all objects in a bucket, specify an empty string\. To filter using a V1 replication configuration, add the `Prefix` directly as a child element of the `Rule` element\.  
Replacement must be made for object keys containing special characters \(such as carriage returns\) when using XML requests\. For more information, see [ XML related object key constraints](https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-keys.html#object-key-xml-related-constraints)\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Priority`  <a name="cfn-s3-bucket-replicationrule-priority"></a>
The priority indicates which rule has precedence whenever two or more replication rules conflict\. Amazon S3 will attempt to replicate objects according to all replication rules\. However, if there are two or more rules with the same destination bucket, then objects will be replicated according to the rule with the highest priority\. The higher the number, the higher the priority\.   
For more information, see [Replication](https://docs.aws.amazon.com/AmazonS3/latest/dev/replication.html) in the *Amazon S3 User Guide*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceSelectionCriteria`  <a name="cfn-s3-bucket-replicationrule-sourceselectioncriteria"></a>
A container that describes additional filters for identifying the source objects that you want to replicate\. You can choose to enable or disable the replication of these objects\.  
*Required*: No  
*Type*: [SourceSelectionCriteria](aws-properties-s3-bucket-sourceselectioncriteria.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-s3-bucket-replicationconfiguration-rules-status"></a>
Specifies whether the rule is enabled\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Disabled | Enabled`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-s3-bucket-replicationconfiguration-rules--examples"></a>



### Associate a replication configuration IAM role with an S3 bucket<a name="aws-properties-s3-bucket-replicationconfiguration-rules--examples--Associate_a_replication_configuration_IAM_role_with_an_S3_bucket"></a>

The following example creates an S3 bucket and grants it permission to write to a replication bucket by using an AWS Identity and Access Management \(IAM\) role\. To avoid a circular dependency, the role's policy is declared as a separate resource\. The bucket depends on the `WorkItemBucketBackupRole` role\. If the policy is included in the role, the role also depends on the bucket\.

#### JSON<a name="aws-properties-s3-bucket-replicationconfiguration-rules--examples--Associate_a_replication_configuration_IAM_role_with_an_S3_bucket--json"></a>

```
{
    "Resources": {
        "RecordServiceS3Bucket": {
            "Type": "AWS::S3::Bucket",
            "DeletionPolicy": "Retain",
            "Properties": {
                "ReplicationConfiguration": {
                    "Role": {
                        "Fn::GetAtt": [
                            "WorkItemBucketBackupRole",
                            "Arn"
                        ]
                    },
                    "Rules": [
                        {
                            "Destination": {
                                "Bucket": {
                                    "Fn::Join": [
                                        "",
                                        [
                                            "arn:aws:s3:::",
                                            {
                                                "Fn::Join": [
                                                    "-",
                                                    [
                                                        {
                                                            "Ref": "AWS::Region"
                                                        },
                                                        {
                                                            "Ref": "AWS::StackName"
                                                        },
                                                        "replicationbucket"
                                                    ]
                                                ]
                                            }
                                        ]
                                    ]
                                },
                                "StorageClass": "STANDARD"
                            },
                            "Id": "Backup",
                            "Prefix": "",
                            "Status": "Enabled"
                        }
                    ]
                },
                "VersioningConfiguration": {
                    "Status": "Enabled"
                }
            }
        },
        "WorkItemBucketBackupRole": {
            "Type": "AWS::IAM::Role",
            "Properties": {
                "AssumeRolePolicyDocument": {
                    "Statement": [
                        {
                            "Action": [
                                "sts:AssumeRole"
                            ],
                            "Effect": "Allow",
                            "Principal": {
                                "Service": [
                                    "s3.amazonaws.com"
                                ]
                            }
                        }
                    ]
                }
            }
        },
        "BucketBackupPolicy": {
            "Type": "AWS::IAM::Policy",
            "Properties": {
                "PolicyDocument": {
                    "Statement": [
                        {
                            "Action": [
                                "s3:GetReplicationConfiguration",
                                "s3:ListBucket"
                            ],
                            "Effect": "Allow",
                            "Resource": [
                                {
                                    "Fn::Join": [
                                        "",
                                        [
                                            "arn:aws:s3:::",
                                            {
                                                "Ref": "RecordServiceS3Bucket"
                                            }
                                        ]
                                    ]
                                }
                            ]
                        },
                        {
                            "Action": [
                                "s3:GetObjectVersion",
                                "s3:GetObjectVersionAcl"
                            ],
                            "Effect": "Allow",
                            "Resource": [
                                {
                                    "Fn::Join": [
                                        "",
                                        [
                                            "arn:aws:s3:::",
                                            {
                                                "Ref": "RecordServiceS3Bucket"
                                            },
                                            "/*"
                                        ]
                                    ]
                                }
                            ]
                        },
                        {
                            "Action": [
                                "s3:ReplicateObject",
                                "s3:ReplicateDelete"
                            ],
                            "Effect": "Allow",
                            "Resource": [
                                {
                                    "Fn::Join": [
                                        "",
                                        [
                                            "arn:aws:s3:::",
                                            {
                                                "Fn::Join": [
                                                    "-",
                                                    [
                                                        {
                                                            "Ref": "AWS::Region"
                                                        },
                                                        {
                                                            "Ref": "AWS::StackName"
                                                        },
                                                        "replicationbucket"
                                                    ]
                                                ]
                                            },
                                            "/*"
                                        ]
                                    ]
                                }
                            ]
                        }
                    ]
                },
                "PolicyName": "BucketBackupPolicy",
                "Roles": [
                    {
                        "Ref": "WorkItemBucketBackupRole"
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-properties-s3-bucket-replicationconfiguration-rules--examples--Associate_a_replication_configuration_IAM_role_with_an_S3_bucket--yaml"></a>

```
Resources:
  RecordServiceS3Bucket:
    Type: 'AWS::S3::Bucket'
    DeletionPolicy: Retain
    Properties:
      ReplicationConfiguration:
        Role: !GetAtt
          - WorkItemBucketBackupRole
          - Arn
        Rules:
          - Destination:
              Bucket: !Join
                - ''
                - - 'arn:aws:s3:::'
                  - !Join
                    - '-'
                    - - !Ref 'AWS::Region'
                      - !Ref 'AWS::StackName'
                      - replicationbucket
              StorageClass: STANDARD
            Id: Backup
            Prefix: ''
            Status: Enabled
      VersioningConfiguration:
        Status: Enabled
  WorkItemBucketBackupRole:
    Type: 'AWS::IAM::Role'
    Properties:
      AssumeRolePolicyDocument:
        Statement:
          - Action:
              - 'sts:AssumeRole'
            Effect: Allow
            Principal:
              Service:
                - s3.amazonaws.com
  BucketBackupPolicy:
    Type: 'AWS::IAM::Policy'
    Properties:
      PolicyDocument:
        Statement:
          - Action:
              - 's3:GetReplicationConfiguration'
              - 's3:ListBucket'
            Effect: Allow
            Resource:
              - !Join
                - ''
                - - 'arn:aws:s3:::'
                  - !Ref RecordServiceS3Bucket
          - Action:
              - 's3:GetObjectVersion'
              - 's3:GetObjectVersionAcl'
            Effect: Allow
            Resource:
              - !Join
                - ''
                - - 'arn:aws:s3:::'
                  - !Ref RecordServiceS3Bucket
                  - /*
          - Action:
              - 's3:ReplicateObject'
              - 's3:ReplicateDelete'
            Effect: Allow
            Resource:
              - !Join
                - ''
                - - 'arn:aws:s3:::'
                  - !Join
                    - '-'
                    - - !Ref 'AWS::Region'
                      - !Ref 'AWS::StackName'
                      - replicationbucket
                  - /*
      PolicyName: BucketBackupPolicy
      Roles:
        - !Ref WorkItemBucketBackupRole
```

### Enable versioning and replicate objects<a name="aws-properties-s3-bucket-replicationconfiguration-rules--examples--Enable_versioning_and_replicate_objects"></a>

The following example enables versioning and two replication rules\. The rules copy objects prefixed with either `MyPrefix` and `MyOtherPrefix` and stores the copied objects in a bucket named `my-replication-bucket`\.

#### JSON<a name="aws-properties-s3-bucket-replicationconfiguration-rules--examples--Enable_versioning_and_replicate_objects--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "S3Bucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "VersioningConfiguration": {
                    "Status": "Enabled"
                },
                "ReplicationConfiguration": {
                    "Role": "arn:aws:iam::123456789012:role/replication_role",
                    "Rules": [
                        {
                            "Id": "MyRule1",
                            "Status": "Enabled",
                            "Prefix": "MyPrefix",
                            "Destination": {
                                "Bucket": "arn:aws:s3:::my-replication-bucket",
                                "StorageClass": "STANDARD"
                            }
                        },
                        {
                            "Status": "Enabled",
                            "Prefix": "MyOtherPrefix",
                            "Destination": {
                                "Bucket": "arn:aws:s3:::my-replication-bucket"
                            }
                        }
                    ]
                }
            }
        }
    }
}
```

#### YAML<a name="aws-properties-s3-bucket-replicationconfiguration-rules--examples--Enable_versioning_and_replicate_objects--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  S3Bucket:
    Type: 'AWS::S3::Bucket'
    Properties:
      VersioningConfiguration:
        Status: Enabled
      ReplicationConfiguration:
        Role: 'arn:aws:iam::123456789012:role/replication_role'
        Rules:
          - Id: MyRule1
            Status: Enabled
            Prefix: MyPrefix
            Destination:
              Bucket: 'arn:aws:s3:::my-replication-bucket'
              StorageClass: STANDARD
          - Status: Enabled
            Prefix: MyOtherPrefix
            Destination:
              Bucket: 'arn:aws:s3:::my-replication-bucket'
```