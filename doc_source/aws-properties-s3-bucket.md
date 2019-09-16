# AWS::S3::Bucket<a name="aws-properties-s3-bucket"></a>

The `AWS::S3::Bucket` resource creates an Amazon S3 bucket in the same AWS Region where you create the AWS CloudFormation stack\.

To control how AWS CloudFormation handles the bucket when the stack is deleted, you can set a deletion policy for your bucket\. You can choose to *retain* the bucket or to *delete* the bucket\. For more information, see [DeletionPolicy Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-deletionpolicy.html)\.

**Important**  
You can only delete empty buckets\. Deletion fails for buckets that have contents\.

## Syntax<a name="aws-properties-s3-bucket-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-syntax.json"></a>

```
{
  "Type" : "AWS::S3::Bucket",
  "Properties" : {
      "[AccelerateConfiguration](#cfn-s3-bucket-accelerateconfiguration)" : [AccelerateConfiguration](aws-properties-s3-bucket-accelerateconfiguration.md),
      "[AccessControl](#cfn-s3-bucket-accesscontrol)" : String,
      "[AnalyticsConfigurations](#cfn-s3-bucket-analyticsconfigurations)" : [ [AnalyticsConfiguration](aws-properties-s3-bucket-analyticsconfiguration.md), ... ],
      "[BucketEncryption](#cfn-s3-bucket-bucketencryption)" : [BucketEncryption](aws-properties-s3-bucket-bucketencryption.md),
      "[BucketName](#cfn-s3-bucket-name)" : String,
      "[CorsConfiguration](#cfn-s3-bucket-crossoriginconfig)" : [CorsConfiguration](aws-properties-s3-bucket-cors.md),
      "[InventoryConfigurations](#cfn-s3-bucket-inventoryconfigurations)" : [ [InventoryConfiguration](aws-properties-s3-bucket-inventoryconfiguration.md), ... ],
      "[LifecycleConfiguration](#cfn-s3-bucket-lifecycleconfig)" : [LifecycleConfiguration](aws-properties-s3-bucket-lifecycleconfig.md),
      "[LoggingConfiguration](#cfn-s3-bucket-loggingconfig)" : [LoggingConfiguration](aws-properties-s3-bucket-loggingconfig.md),
      "[MetricsConfigurations](#cfn-s3-bucket-metricsconfigurations)" : [ [MetricsConfiguration](aws-properties-s3-bucket-metricsconfiguration.md), ... ],
      "[NotificationConfiguration](#cfn-s3-bucket-notification)" : [NotificationConfiguration](aws-properties-s3-bucket-notificationconfig.md),
      "[ObjectLockConfiguration](#cfn-s3-bucket-objectlockconfiguration)" : [ObjectLockConfiguration](aws-properties-s3-bucket-objectlockconfiguration.md),
      "[ObjectLockEnabled](#cfn-s3-bucket-objectlockenabled)" : Boolean,
      "[PublicAccessBlockConfiguration](#cfn-s3-bucket-publicaccessblockconfiguration)" : [PublicAccessBlockConfiguration](aws-properties-s3-bucket-publicaccessblockconfiguration.md),
      "[ReplicationConfiguration](#cfn-s3-bucket-replicationconfiguration)" : [ReplicationConfiguration](aws-properties-s3-bucket-replicationconfiguration.md),
      "[Tags](#cfn-s3-bucket-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VersioningConfiguration](#cfn-s3-bucket-versioning)" : [VersioningConfiguration](aws-properties-s3-bucket-versioningconfig.md),
      "[WebsiteConfiguration](#cfn-s3-bucket-websiteconfiguration)" : [WebsiteConfiguration](aws-properties-s3-websiteconfiguration.md)
    }
}
```

### YAML<a name="aws-properties-s3-bucket-syntax.yaml"></a>

```
Type: AWS::S3::Bucket
Properties: 
  [AccelerateConfiguration](#cfn-s3-bucket-accelerateconfiguration): 
    [AccelerateConfiguration](aws-properties-s3-bucket-accelerateconfiguration.md)
  [AccessControl](#cfn-s3-bucket-accesscontrol): String
  [AnalyticsConfigurations](#cfn-s3-bucket-analyticsconfigurations): 
    - [AnalyticsConfiguration](aws-properties-s3-bucket-analyticsconfiguration.md)
  [BucketEncryption](#cfn-s3-bucket-bucketencryption): 
    [BucketEncryption](aws-properties-s3-bucket-bucketencryption.md)
  [BucketName](#cfn-s3-bucket-name): String
  [CorsConfiguration](#cfn-s3-bucket-crossoriginconfig): 
    [CorsConfiguration](aws-properties-s3-bucket-cors.md)
  [InventoryConfigurations](#cfn-s3-bucket-inventoryconfigurations): 
    - [InventoryConfiguration](aws-properties-s3-bucket-inventoryconfiguration.md)
  [LifecycleConfiguration](#cfn-s3-bucket-lifecycleconfig): 
    [LifecycleConfiguration](aws-properties-s3-bucket-lifecycleconfig.md)
  [LoggingConfiguration](#cfn-s3-bucket-loggingconfig): 
    [LoggingConfiguration](aws-properties-s3-bucket-loggingconfig.md)
  [MetricsConfigurations](#cfn-s3-bucket-metricsconfigurations): 
    - [MetricsConfiguration](aws-properties-s3-bucket-metricsconfiguration.md)
  [NotificationConfiguration](#cfn-s3-bucket-notification): 
    [NotificationConfiguration](aws-properties-s3-bucket-notificationconfig.md)
  [ObjectLockConfiguration](#cfn-s3-bucket-objectlockconfiguration): 
    [ObjectLockConfiguration](aws-properties-s3-bucket-objectlockconfiguration.md)
  [ObjectLockEnabled](#cfn-s3-bucket-objectlockenabled): Boolean
  [PublicAccessBlockConfiguration](#cfn-s3-bucket-publicaccessblockconfiguration): 
    [PublicAccessBlockConfiguration](aws-properties-s3-bucket-publicaccessblockconfiguration.md)
  [ReplicationConfiguration](#cfn-s3-bucket-replicationconfiguration): 
    [ReplicationConfiguration](aws-properties-s3-bucket-replicationconfiguration.md)
  [Tags](#cfn-s3-bucket-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VersioningConfiguration](#cfn-s3-bucket-versioning): 
    [VersioningConfiguration](aws-properties-s3-bucket-versioningconfig.md)
  [WebsiteConfiguration](#cfn-s3-bucket-websiteconfiguration): 
    [WebsiteConfiguration](aws-properties-s3-websiteconfiguration.md)
```

## Properties<a name="aws-properties-s3-bucket-properties"></a>

`AccelerateConfiguration`  <a name="cfn-s3-bucket-accelerateconfiguration"></a>
Configures the transfer acceleration state for an Amazon S3 bucket\. For more information, see [Amazon S3 Transfer Acceleration](https://docs.aws.amazon.com/AmazonS3/latest/dev/transfer-acceleration.html) in the *Amazon Simple Storage Service Developer Guide*\.  
*Required*: No  
*Type*: [AccelerateConfiguration](aws-properties-s3-bucket-accelerateconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AccessControl`  <a name="cfn-s3-bucket-accesscontrol"></a>
A canned access control list \(ACL\) that grants predefined permissions to the bucket\. For more information about canned ACLs, see [Canned ACL](https://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html#canned-acl) in the *Amazon Simple Storage Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AnalyticsConfigurations`  <a name="cfn-s3-bucket-analyticsconfigurations"></a>
 Specifies the configuration and any analyses for the analytics filter of an Amazon S3 bucket\.  
For more information, see [GET Bucket analytics](https://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketGETAnalyticsConfig.html) in the *Amazon Simple Storage Service API Reference*\.   
*Required*: No  
*Type*: List of [AnalyticsConfiguration](aws-properties-s3-bucket-analyticsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BucketEncryption`  <a name="cfn-s3-bucket-bucketencryption"></a>
Specifies default encryption for a bucket using server\-side encryption with Amazon S3\-managed keys \(SSE\-S3\) or AWS KMS\-managed keys \(SSE\-KMS\) bucket\. For information about the Amazon S3 default encryption feature, see [ Amazon S3 Default Encryption for S3 Buckets](https://docs.aws.amazon.com/AmazonS3/latest/dev/bucket-encryption.html) in the *Amazon Simple Storage Service Developer Guide*\.  
*Required*: No  
*Type*: [BucketEncryption](aws-properties-s3-bucket-bucketencryption.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BucketName`  <a name="cfn-s3-bucket-name"></a>
A name for the bucket\. If you don't specify a name, AWS CloudFormation generates a unique ID and uses that ID for the bucket name\. For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\. The bucket name must contain only lowercase letters, numbers, periods \(\.\), and dashes \(\-\)\.  
If you specify a name, you can't perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you need to replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CorsConfiguration`  <a name="cfn-s3-bucket-crossoriginconfig"></a>
Describes the cross\-origin access configuration for objects in an Amazon S3 bucket\. For more information, see [Enabling Cross\-Origin Resource Sharing](https://docs.aws.amazon.com/AmazonS3/latest/dev/cors.html) in the *Amazon Simple Storage Service Developer Guide*\.  
*Required*: No  
*Type*: [CorsConfiguration](aws-properties-s3-bucket-cors.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InventoryConfigurations`  <a name="cfn-s3-bucket-inventoryconfigurations"></a>
Specifies the inventory configuration for an Amazon S3 bucket\. For more information, see [GET Bucket inventory](https://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketGETInventoryConfig.html) in the *Amazon Simple Storage Service API Reference*\.   
*Required*: No  
*Type*: List of [InventoryConfiguration](aws-properties-s3-bucket-inventoryconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LifecycleConfiguration`  <a name="cfn-s3-bucket-lifecycleconfig"></a>
Specifies the lifecycle configuration for objects in an Amazon S3 bucket\. For more information, see [Object Lifecycle Management](https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lifecycle-mgmt.html) in the *Amazon Simple Storage Service Developer Guide*\.  
*Required*: No  
*Type*: [LifecycleConfiguration](aws-properties-s3-bucket-lifecycleconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoggingConfiguration`  <a name="cfn-s3-bucket-loggingconfig"></a>
Settings that define where logs are stored\.  
*Required*: No  
*Type*: [LoggingConfiguration](aws-properties-s3-bucket-loggingconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricsConfigurations`  <a name="cfn-s3-bucket-metricsconfigurations"></a>
Specifies a metrics configuration for the CloudWatch request metrics \(specified by the metrics configuration ID\) from an Amazon S3 bucket\. If you're updating an existing metrics configuration, note that this is a full replacement of the existing metrics configuration\. If you don't include the elements you want to keep, they are erased\. For more information, see [ PUT Bucket metrics](https://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUTMetricConfiguration.html) in the *Amazon Simple Storage Service API Reference*\.  
*Required*: No  
*Type*: List of [MetricsConfiguration](aws-properties-s3-bucket-metricsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotificationConfiguration`  <a name="cfn-s3-bucket-notification"></a>
Configuration that defines how Amazon S3 handles bucket notifications\.  
*Required*: No  
*Type*: [NotificationConfiguration](aws-properties-s3-bucket-notificationconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObjectLockConfiguration`  <a name="cfn-s3-bucket-objectlockconfiguration"></a>
Places an object lock configuration on the specified bucket\. The rule specified in the object lock configuration will be applied by default to every new object placed in the specified bucket\.  
*Required*: No  
*Type*: [ObjectLockConfiguration](aws-properties-s3-bucket-objectlockconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObjectLockEnabled`  <a name="cfn-s3-bucket-objectlockenabled"></a>
Indicates whether this bucket has an object lock configuration enabled\.  
*Required*: No  
*Type*: Boolean  
*Allowed Values*: `Enabled`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PublicAccessBlockConfiguration`  <a name="cfn-s3-bucket-publicaccessblockconfiguration"></a>
Configuration that defines how Amazon S3 handles public access\.  
*Required*: No  
*Type*: [PublicAccessBlockConfiguration](aws-properties-s3-bucket-publicaccessblockconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplicationConfiguration`  <a name="cfn-s3-bucket-replicationconfiguration"></a>
Configuration for replicating objects in an S3 bucket\. To enable replication, you must also enable versioning by using the `VersioningConfiguration` property\.  
Amazon S3 can store replicated objects in only one destination bucket\. The destination bucket must already exist and be in a different AWS Region than your source bucket\.  
*Required*: No  
*Type*: [ReplicationConfiguration](aws-properties-s3-bucket-replicationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-s3-bucket-tags"></a>
An arbitrary set of tags \(key\-value pairs\) for this S3 bucket\.  
 We recommend limiting the number of tags to seven\. Applying more than seven tags prevents the AWS CLI and the AWS CloudFormation console and API actions from listing the tags for the bucket\. 
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VersioningConfiguration`  <a name="cfn-s3-bucket-versioning"></a>
Enables multiple versions of all objects in this bucket\. You might enable versioning to prevent objects from being deleted or overwritten by mistake or to archive objects so that you can retrieve previous versions of them\.  
*Required*: No  
*Type*: [VersioningConfiguration](aws-properties-s3-bucket-versioningconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WebsiteConfiguration`  <a name="cfn-s3-bucket-websiteconfiguration"></a>
Information used to configure the bucket as a static website\. For more information, see [Hosting Websites on Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/dev/WebsiteHosting.html)\.  
*Required*: No  
*Type*: [WebsiteConfiguration](aws-properties-s3-websiteconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-properties-s3-bucket-return-values"></a>

### Ref<a name="aws-properties-s3-bucket-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

Example: `mystack-mybucket-kdwwxmddtr2g` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-properties-s3-bucket-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-properties-s3-bucket-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) of the specified bucket\.  
Example: `arn:aws:s3:::mybucket` 

`DomainName`  <a name="DomainName-fn::getatt"></a>
Returns the IPv4 DNS name of the specified bucket\.  
Example: `mystack-mybucket-kdwwxmddtr2g.s3.amazonaws.com` 

`DualStackDomainName`  <a name="DualStackDomainName-fn::getatt"></a>
Returns the IPv6 DNS name of the specified bucket\.  
Example: ` mystack-mybucket-kdwwxmddtr2g.s3.dualstack.us-east-2.amazonaws.com`   
For more information about dual\-stack endpoints, see [Using Amazon S3 Dual\-Stack Endpoints](https://docs.aws.amazon.com/AmazonS3/latest/dev/dual-stack-endpoints.html)\.

`RegionalDomainName`  <a name="RegionalDomainName-fn::getatt"></a>
Returns the regional domain name of the specified bucket\.  
Example: `mystack-mybucket-kdwwxmddtr2g.s3.us-east-2.amazonaws.com` 

`WebsiteURL`  <a name="WebsiteURL-fn::getatt"></a>
Returns the Amazon S3 website endpoint for the specified bucket\.  
Example \(IPv4\): `http://mystack-mybucket-kdwwxmddtr2g.s3-website-us-east-2.amazonaws.com/`   
Example \(IPv6\): `http://mystack-mybucket-kdwwxmddtr2g.s3.dualstack.us-east-2.amazonaws.com/` 

## Examples<a name="aws-properties-s3-bucket--examples"></a>

### Associate a Replication Configuration IAM Role with an S3 Bucket<a name="aws-properties-s3-bucket--examples--Associate_a_Replication_Configuration_IAM_Role_with_an_S3_Bucket"></a>

The following example creates an S3 bucket and grants it permission to write to a replication bucket by using an AWS Identity and Access Management \(IAM\) role\. To avoid a circular dependency, the role's policy is declared as a separate resource\. The bucket depends on the `WorkItemBucketBackupRole` role\. If the policy is included in the role, the role also depends on the bucket\.

#### JSON<a name="aws-properties-s3-bucket--examples--Associate_a_Replication_Configuration_IAM_Role_with_an_S3_Bucket--json"></a>

```
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
      "Rules": [{
        "Destination": {
          "Bucket": {
            "Fn::Join": [ "", [
              "arn:aws:s3:::", {
                "Fn::Join": [ "-", [
                  { "Ref": "AWS::Region" },
                  { "Ref": "AWS::StackName" },
                  "replicationbucket"
                ]]
              }
            ]]
          },
          "StorageClass": "STANDARD"
        },
        "Id": "Backup",
        "Prefix": "",
        "Status": "Enabled"
      }]
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
      "Statement": [{
        "Action": [ "sts:AssumeRole" ],
        "Effect": "Allow",
        "Principal": {
          "Service": [ "s3.amazonaws.com" ]
        }
      }]
    }
  }    
},
"BucketBackupPolicy": {
  "Type": "AWS::IAM::Policy",
  "Properties": {
    "PolicyDocument": {
      "Statement": [{
        "Action": [
          "s3:GetReplicationConfiguration",
          "s3:ListBucket"
        ],
        "Effect": "Allow",
        "Resource": [{
          "Fn::Join": [ "", [
              "arn:aws:s3:::", {
                "Ref": "RecordServiceS3Bucket"
              }
            ]
          ]
        }]
      },{
        "Action": [
          "s3:GetObjectVersion",
          "s3:GetObjectVersionAcl"
        ],
        "Effect": "Allow",
        "Resource": [{
          "Fn::Join": [ "", [
              "arn:aws:s3:::", {
                "Ref": "RecordServiceS3Bucket"
              },
              "/*"
            ]
          ]
        }]
      }, {
        "Action": [
          "s3:ReplicateObject",
          "s3:ReplicateDelete"
        ],
        "Effect": "Allow",
        "Resource": [{
          "Fn::Join": [ "", [ 
             "arn:aws:s3:::", {
               "Fn::Join": [ "-", [ 
                 { "Ref": "AWS::Region" }, 
                 { "Ref": "AWS::StackName" }, 
                 "replicationbucket"
               ]]
             }, 
             "/*"
          ]]
        }]
      }]
    },
    "PolicyName": "BucketBackupPolicy",
    "Roles": [{
      "Ref": "WorkItemBucketBackupRole"
    }]
  }
}
```

#### YAML<a name="aws-properties-s3-bucket--examples--Associate_a_Replication_Configuration_IAM_Role_with_an_S3_Bucket--yaml"></a>

```
RecordServiceS3Bucket:
  Type: AWS::S3::Bucket
  DeletionPolicy: Retain
  Properties:
    ReplicationConfiguration:
      Role: !GetAtt [WorkItemBucketBackupRole, Arn]
      Rules:
      - Destination:
          Bucket: !Join ['', ['arn:aws:s3:::', !Join ['-', [!Ref 'AWS::Region', !Ref 'AWS::StackName',
                  replicationbucket]]]]
          StorageClass: STANDARD
        Id: Backup
        Prefix: ''
        Status: Enabled
    VersioningConfiguration:
      Status: Enabled
WorkItemBucketBackupRole:
  Type: AWS::IAM::Role
  Properties:
    AssumeRolePolicyDocument:
      Statement:
      - Action: ['sts:AssumeRole']
        Effect: Allow
        Principal:
          Service: [s3.amazonaws.com]
BucketBackupPolicy:
  Type: AWS::IAM::Policy
  Properties:
    PolicyDocument:
      Statement:
      - Action: ['s3:GetReplicationConfiguration', 's3:ListBucket']
        Effect: Allow
        Resource:
        - !Join ['', ['arn:aws:s3:::', !Ref 'RecordServiceS3Bucket']]
      - Action: ['s3:GetObjectVersion', 's3:GetObjectVersionAcl']
        Effect: Allow
        Resource:
        - !Join ['', ['arn:aws:s3:::', !Ref 'RecordServiceS3Bucket', /*]]
      - Action: ['s3:ReplicateObject', 's3:ReplicateDelete']
        Effect: Allow
        Resource:
        - !Join ['', ['arn:aws:s3:::', !Join ['-', [!Ref 'AWS::Region', !Ref 'AWS::StackName',
                replicationbucket]], /*]]
    PolicyName: BucketBackupPolicy
    Roles: [!Ref 'WorkItemBucketBackupRole']
```

### Configure a Static Website with a Routing Rule<a name="aws-properties-s3-bucket--examples--Configure_a_Static_Website_with_a_Routing_Rule"></a>

In this example, `AWS::S3::Bucket's Fn::GetAtt` values are used to provide outputs\. If an HTTP 404 error occurs, the routing rule redirects requests to an EC2 instance and inserts the object key prefix `report-404/` in the redirect\. For example, if you request a page called `ExamplePage.html` and it results in an HTTP 404 error, the request is routed to a page called `report-404/ExamplePage.html` on the specified instance\. For all other HTTP error codes, `error.html` is returned\. 

This example also specifies a metrics configuration called `EntireBucket` that enables CloudWatch request metrics at the bucket level\.

#### JSON<a name="aws-properties-s3-bucket--examples--Configure_a_Static_Website_with_a_Routing_Rule--json"></a>

```
"Resources" : {
   "S3Bucket" : {
      "Type" : "AWS::S3::Bucket",
      "Properties" : {
         "AccessControl" : "PublicRead",
         "BucketName" : "public-bucket",
         "MetricsConfigurations": [
            {
               "Id": "EntireBucket"
            }
         ],
         "WebsiteConfiguration" : {
            "IndexDocument" : "index.html",
            "ErrorDocument" : "error.html",
            "RoutingRules": [
                {
                    "RoutingRuleCondition": {
                        "HttpErrorCodeReturnedEquals": "404",
                        "KeyPrefixEquals": "out1/"
                    },
                    "RedirectRule": {
                        "HostName": "ec2-11-22-333-44.compute-1.amazonaws.com",
                        "ReplaceKeyPrefixWith": "report-404/"
                    }
                }
            ]
         }
      },
      "DeletionPolicy" : "Retain"
   }
},

"Outputs" : {
   "WebsiteURL" : {
      "Value" : { "Fn::GetAtt" : [ "S3Bucket", "WebsiteURL" ] },
      "Description" : "URL for website hosted on S3"
   },
   "S3BucketSecureURL" : {
      "Value" : { "Fn::Join" : [
         "", [ "https://", { "Fn::GetAtt" : [ "S3Bucket", "DomainName" ] } ]
      ] },
      "Description" : "Name of S3 bucket to hold website content"
   }
}
```

#### YAML<a name="aws-properties-s3-bucket--examples--Configure_a_Static_Website_with_a_Routing_Rule--yaml"></a>

```
Resources:
  S3Bucket:
    Type: AWS::S3::Bucket
    Properties:
      AccessControl: PublicRead
      BucketName: public-bucket
      MetricsConfigurations: 
        - Id: EntireBucket
      WebsiteConfiguration:
        IndexDocument: index.html
        ErrorDocument: error.html
        RoutingRules:
        - RoutingRuleCondition:
            HttpErrorCodeReturnedEquals: '404'
            KeyPrefixEquals: out1/
          RedirectRule:
            HostName: ec2-11-22-333-44.compute-1.amazonaws.com
            ReplaceKeyPrefixWith: report-404/
    DeletionPolicy: Retain
Outputs:
  WebsiteURL:
    Value: !GetAtt [S3Bucket, WebsiteURL]
    Description: URL for website hosted on S3
  S3BucketSecureURL:
    Value: !Join ['', ['https://', !GetAtt [S3Bucket, DomainName]]]
    Description: Name of S3 bucket to hold website content
```

### Enable Cross\-Origin Resource Sharing<a name="aws-properties-s3-bucket--examples--Enable_Cross-Origin_Resource_Sharing"></a>

The following example template shows an S3 bucket with two cross\-origin resource sharing rules\.

#### JSON<a name="aws-properties-s3-bucket--examples--Enable_Cross-Origin_Resource_Sharing--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Resources": {
        "S3Bucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "AccessControl": "PublicReadWrite",
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
                            "MaxAge": "3600"
                        },
                        {
                            "AllowedHeaders": [
                                "x-amz-*"
                            ],
                            "AllowedMethods": [
                                "DELETE"
                            ],
                            "AllowedOrigins": [
                                "http://www.example1.com",
                                "http://www.example2.com"
                            ],
                            "ExposedHeaders": [
                                "Connection",
                                "Server",
                                "Date"
                            ],
                            "Id": "myCORSRuleId2",
                            "MaxAge": "1800"
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

#### YAML<a name="aws-properties-s3-bucket--examples--Enable_Cross-Origin_Resource_Sharing--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  S3Bucket:
    Type: AWS::S3::Bucket
    Properties:
      AccessControl: PublicReadWrite
      CorsConfiguration:
        CorsRules:
        - AllowedHeaders: ['*']
          AllowedMethods: [GET]
          AllowedOrigins: ['*']
          ExposedHeaders: [Date]
          Id: myCORSRuleId1
          MaxAge: '3600'
        - AllowedHeaders: [x-amz-*]
          AllowedMethods: [DELETE]
          AllowedOrigins: ['http://www.example1.com', 'http://www.example2.com']
          ExposedHeaders: [Connection, Server, Date]
          Id: myCORSRuleId2
          MaxAge: '1800'
Outputs:
  BucketName:
    Value: !Ref 'S3Bucket'
    Description: Name of the sample Amazon S3 bucket with CORS enabled.
```

### Manage the Lifecycle for Amazon S3 Objects<a name="aws-properties-s3-bucket--examples--Manage_the_Lifecycle_for_Amazon_S3_Objects"></a>

The following example template shows an S3 bucket with a lifecycle configuration rule\. The rule applies to all objects with the `glacier` key prefix\. The objects are transitioned to Glacier after one day, and deleted after one year\.

#### JSON<a name="aws-properties-s3-bucket--examples--Manage_the_Lifecycle_for_Amazon_S3_Objects--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "S3Bucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "AccessControl": "PublicReadWrite",
                "LifecycleConfiguration": {
                    "Rules": [
                        {
                            "Id": "GlacierRule",
                            "Prefix": "glacier",
                            "Status": "Enabled",
                            "ExpirationInDays": "365",
                            "Transitions": [
                                {
                                  "TransitionInDays": "1",
                                  "StorageClass": "Glacier"
                                }
                            ]
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
            "Description": "Name of the sample Amazon S3 bucket with a lifecycle configuration."
        }
    }
}
```

#### YAML<a name="aws-properties-s3-bucket--examples--Manage_the_Lifecycle_for_Amazon_S3_Objects--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  S3Bucket:
    Type: AWS::S3::Bucket
    Properties:
      AccessControl: PublicReadWrite
      LifecycleConfiguration:
        Rules:
        - Id: GlacierRule
          Prefix: glacier
          Status: Enabled
          ExpirationInDays: '365'
          Transitions:
            - TransitionInDays: '1'
              StorageClass: Glacier
Outputs:
  BucketName:
    Value: !Ref 'S3Bucket'
    Description: Name of the sample Amazon S3 bucket with a lifecycle configuration.
```

### Log Access Requests for a Specific S3 Bucket<a name="aws-properties-s3-bucket--examples--Log_Access_Requests_for_a_Specific_S3_Bucket"></a>

The following example template creates two S3 buckets\. The `LoggingBucket` bucket store the logs from the `S3Bucket` bucket\. To receive logs from the `S3Bucket` bucket, the logging bucket requires log delivery write permissions\.

#### JSON<a name="aws-properties-s3-bucket--examples--Log_Access_Requests_for_a_Specific_S3_Bucket--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "S3Bucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "AccessControl": "PublicRead",
                "LoggingConfiguration": {
                    "DestinationBucketName": {"Ref" : "LoggingBucket"},
                    "LogFilePrefix": "testing-logs"
                }
            }
        },
        "LoggingBucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "AccessControl": "LogDeliveryWrite"
            }
        }
    },
    "Outputs": {
        "BucketName": {
            "Value": {
                "Ref": "S3Bucket"
            },
            "Description": "Name of the sample Amazon S3 bucket with a logging configuration."
        }
    }
}
```

#### YAML<a name="aws-properties-s3-bucket--examples--Log_Access_Requests_for_a_Specific_S3_Bucket--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  S3Bucket:
    Type: AWS::S3::Bucket
    Properties:
      AccessControl: PublicRead
      LoggingConfiguration:
        DestinationBucketName: !Ref 'LoggingBucket'
        LogFilePrefix: testing-logs
  LoggingBucket:
    Type: AWS::S3::Bucket
    Properties:
      AccessControl: LogDeliveryWrite
Outputs:
  BucketName:
    Value: !Ref 'S3Bucket'
    Description: Name of the sample Amazon S3 bucket with a logging configuration.
```

### Receive S3 Bucket Notifications to an SNS Topic<a name="aws-properties-s3-bucket--examples--Receive_S3_Bucket_Notifications_to_an_SNS_Topic"></a>

The following example template shows an Amazon S3 bucket with a notification configuration that sends an event to the specified SNS topic when S3 has lost all replicas of an object\.

#### JSON<a name="aws-properties-s3-bucket--examples--Receive_S3_Bucket_Notifications_to_an_SNS_Topic--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "S3Bucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "AccessControl": "PublicReadWrite",
                "NotificationConfiguration": {
                    "TopicConfigurations": [
                        {
                            "Topic": "arn:aws:sns:us-east-1:123456789012:TestTopic",
                            "Event": "s3:ReducedRedundancyLostObject"
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
            "Description": "Name of the sample Amazon S3 bucket with a notification configuration."
        }
    }
}
```

#### YAML<a name="aws-properties-s3-bucket--examples--Receive_S3_Bucket_Notifications_to_an_SNS_Topic--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  S3Bucket:
    Type: AWS::S3::Bucket
    Properties:
      AccessControl: PublicReadWrite
      NotificationConfiguration:
        TopicConfigurations:
        - Topic: arn:aws:sns:us-east-1:123456789012:TestTopic
          Event: s3:ReducedRedundancyLostObject
Outputs:
  BucketName:
    Value: !Ref 'S3Bucket'
    Description: Name of the sample Amazon S3 bucket with a notification configuration.
```

### Replicate Objects and Store Them in Another S3 Bucket<a name="aws-properties-s3-bucket--examples--Replicate_Objects_and_Store_Them_in_Another_S3_Bucket"></a>

The following example includes two replication rules\. Amazon S3 replicates objects with the `MyPrefix` or `MyOtherPrefix` prefixes and stores them in the `my-replication-bucket` bucket, which must be in a different AWS Region than the `S3Bucket` bucket\.

#### JSON<a name="aws-properties-s3-bucket--examples--Replicate_Objects_and_Store_Them_in_Another_S3_Bucket--json"></a>

```
"S3Bucket": {
  "Type": "AWS::S3::Bucket",
  "Properties": {
    "VersioningConfiguration":{
      "Status":"Enabled"
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
```

#### YAML<a name="aws-properties-s3-bucket--examples--Replicate_Objects_and_Store_Them_in_Another_S3_Bucket--yaml"></a>

```
S3Bucket:
  Type: AWS::S3::Bucket
  Properties:
    VersioningConfiguration:
      Status: Enabled
    ReplicationConfiguration:
      Role: arn:aws:iam::123456789012:role/replication_role
      Rules:
      - Id: MyRule1
        Status: Enabled
        Prefix: MyPrefix
        Destination:
          Bucket: arn:aws:s3:::my-replication-bucket
          StorageClass: STANDARD
      - Status: Enabled
        Prefix: MyOtherPrefix
        Destination:
          Bucket: arn:aws:s3:::my-replication-bucket
```

### Specify Analytics and Inventory Configurations for an Amazon S3 Bucket<a name="aws-properties-s3-bucket--examples--Specify_Analytics_and_Inventory_Configurations_for_an_Amazon_S3_Bucket"></a>

The following example specifies analytics and inventory results to be generated for an S3 bucket, including the format of the results and the bucket to which they are published\. The inventory list is enabled to generate weekly, and only includes the current version of each object\.

#### JSON<a name="aws-properties-s3-bucket--examples--Specify_Analytics_and_Inventory_Configurations_for_an_Amazon_S3_Bucket--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "S3 Bucket with Inventory and Analytics Configurations",
    "Resources": {
        "Helper": {
            "Type": "AWS::S3::Bucket"
        },
        "S3Bucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "AnalyticsConfigurations": [
                    {
                        "Id": "AnalyticsConfigurationId",
                        "StorageClassAnalysis": {
                            "DataExport": {
                                "Destination": {
                                    "BucketArn": {
                                        "Fn::GetAtt": [
                                            "Helper",
                                            "Arn"
                                        ]
                                    },
                                    "Format": "CSV",
                                    "Prefix": "AnalyticsDestinationPrefix"
                                },
                                "OutputSchemaVersion": "V_1"
                            }
                        },
                        "Prefix": "AnalyticsConfigurationPrefix",
                        "TagFilters": [
                            {
                                "Key": "AnalyticsTagKey",
                                "Value": "AnalyticsTagValue"
                            }
                        ]
                    }
                ],
                "InventoryConfigurations": [
                    {
                        "Id": "InventoryConfigurationId",
                        "Destination": {
                            "BucketArn": {
                                "Fn::GetAtt": [
                                    "Helper",
                                    "Arn"
                                ]
                            },
                            "Format": "CSV",
                            "Prefix": "InventoryDestinationPrefix"
                        },
                        "Enabled": "true",
                        "IncludedObjectVersions": "Current",
                        "Prefix": "InventoryConfigurationPrefix",
                        "ScheduleFrequency": "Weekly"
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-properties-s3-bucket--examples--Specify_Analytics_and_Inventory_Configurations_for_an_Amazon_S3_Bucket--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: S3 Bucket with Inventory and Analytics Configurations
Resources:
  Helper:
    Type: AWS::S3::Bucket
  S3Bucket:
    Type: AWS::S3::Bucket
    Properties:
      AnalyticsConfigurations:
        - Id: AnalyticsConfigurationId
          StorageClassAnalysis:
            DataExport:
              Destination:
                BucketArn: !GetAtt 
                  - Helper
                  - Arn
                Format: CSV
                Prefix: AnalyticsDestinationPrefix
              OutputSchemaVersion: V_1
          Prefix: AnalyticsConfigurationPrefix
          TagFilters:
            - Key: AnalyticsTagKey
              Value: AnalyticsTagValue
      InventoryConfigurations:
        - Id: InventoryConfigurationId
          Destination:
            BucketArn: !GetAtt 
              - Helper
              - Arn
            Format: CSV
            Prefix: InventoryDestinationPrefix
          Enabled: 'true'
          IncludedObjectVersions: Current
          Prefix: InventoryConfigurationPrefix
          ScheduleFrequency: Weekly
```

### Create a Bucket with Default Encryption Enabled<a name="aws-properties-s3-bucket--examples--Create_a_Bucket_with_Default_Encryption_Enabled"></a>

The following example creates a bucket with server\-side bucket encryption configured\. This example uses S3\-managed keys\. You can use KMS\-managed keys instead by modifying the [Amazon S3 Bucket ServerSideEncryptionByDefault](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket-serversideencryptionbydefault.html) property\.

#### JSON<a name="aws-properties-s3-bucket--examples--Create_a_Bucket_with_Default_Encryption_Enabled--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "S3 bucket with default encryption",
  "Resources": {
    "EncryptedS3Bucket": {
      "Type": "AWS::S3::Bucket",
      "Properties": {
        "BucketName": {
          "Fn::Sub": "encryptedbucket-${AWS::Region}-${AWS::AccountId}"
        },
        "BucketEncryption": {
          "ServerSideEncryptionConfiguration": [{
            "ServerSideEncryptionByDefault": {
              "SSEAlgorithm": "AES256"
            }
          }]
        }
      },
      "DeletionPolicy": "Delete"
    }
  }
}
```

#### YAML<a name="aws-properties-s3-bucket--examples--Create_a_Bucket_with_Default_Encryption_Enabled--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: S3 bucket with default encryption
Resources:
  EncryptedS3Bucket:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: !Sub 'encryptedbucket-${AWS::Region}-${AWS::AccountId}'
      BucketEncryption:
        ServerSideEncryptionConfiguration:
          - ServerSideEncryptionByDefault:
              SSEAlgorithm: AES256
    DeletionPolicy: Delete
```

## See Also<a name="aws-properties-s3-bucket--seealso"></a>
+ [Amazon S3 Template Snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-s3.html)