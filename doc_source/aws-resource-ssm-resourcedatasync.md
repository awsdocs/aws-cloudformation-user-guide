# AWS::SSM::ResourceDataSync<a name="aws-resource-ssm-resourcedatasync"></a>

The `AWS::SSM::ResourceDataSync` resource creates or deletes a Resource Data Sync for AWS Systems Manager Inventory\. You can use Resource Data Sync to send Inventory data collected from all of your Systems Manager managed instances to a single Amazon S3 bucket that you have already created in your account\. Resource Data Sync then automatically updates the centralized data when new Inventory data is collected\. 

For more information, see [Configuring Inventory Collection](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-inventory-configuring.html#sysman-inventory-datasync) in the *AWS Systems Manager User Guide*\.

## Syntax<a name="aws-resource-ssm-resourcedatasync-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-resourcedatasync-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::ResourceDataSync",
  "Properties" : {
      "[BucketName](#cfn-ssm-resourcedatasync-bucketname)" : String,
      "[BucketPrefix](#cfn-ssm-resourcedatasync-bucketprefix)" : String,
      "[BucketRegion](#cfn-ssm-resourcedatasync-bucketregion)" : String,
      "[KMSKeyArn](#cfn-ssm-resourcedatasync-kmskeyarn)" : String,
      "[SyncFormat](#cfn-ssm-resourcedatasync-syncformat)" : String,
      "[SyncName](#cfn-ssm-resourcedatasync-syncname)" : String
    }
}
```

### YAML<a name="aws-resource-ssm-resourcedatasync-syntax.yaml"></a>

```
Type: AWS::SSM::ResourceDataSync
Properties: 
  [BucketName](#cfn-ssm-resourcedatasync-bucketname): String
  [BucketPrefix](#cfn-ssm-resourcedatasync-bucketprefix): String
  [BucketRegion](#cfn-ssm-resourcedatasync-bucketregion): String
  [KMSKeyArn](#cfn-ssm-resourcedatasync-kmskeyarn): String
  [SyncFormat](#cfn-ssm-resourcedatasync-syncformat): String
  [SyncName](#cfn-ssm-resourcedatasync-syncname): String
```

## Properties<a name="aws-resource-ssm-resourcedatasync-properties"></a>

`BucketName`  <a name="cfn-ssm-resourcedatasync-bucketname"></a>
The name of the Amazon S3 bucket where the aggregated data is stored\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BucketPrefix`  <a name="cfn-ssm-resourcedatasync-bucketprefix"></a>
An Amazon S3 prefix for the bucket\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BucketRegion`  <a name="cfn-ssm-resourcedatasync-bucketregion"></a>
The AWS Region with the Amazon S3 bucket targeted by the Resource Data Sync\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KMSKeyArn`  <a name="cfn-ssm-resourcedatasync-kmskeyarn"></a>
The ARN of an encryption key for a destination in Amazon S3\. You can use a KMS key to encrypt inventory data in Amazon S3\. You must specify a key that exist in the same region as the destination Amazon S3 bucket\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `arn:.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SyncFormat`  <a name="cfn-ssm-resourcedatasync-syncformat"></a>
A supported sync format\. The following format is currently supported: JsonSerDe  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `JsonSerDe`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SyncName`  <a name="cfn-ssm-resourcedatasync-syncname"></a>
A name for the Resource Data Sync\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-ssm-resourcedatasync-return-values"></a>

### Ref<a name="aws-resource-ssm-resourcedatasync-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the Resource Data Sync, such as `TestResourceDataSync`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ssm-resourcedatasync--examples"></a>

### AWS Systems Manager Resource Data Sync<a name="aws-resource-ssm-resourcedatasync--examples--AWS_Systems_Manager_Resource_Data_Sync"></a>

The following examples send Inventory data collected from all of your managed instances in the US East \(Ohio\) Region \(us\-east\-2\) to a single Amazon S3 bucket\. Resource Data Sync then automatically updates the centralized data when new Inventory data is collected\.

#### JSON<a name="aws-resource-ssm-resourcedatasync--examples--AWS_Systems_Manager_Resource_Data_Sync--json"></a>

```
{
  "Description": "Create a Resource Data Sync for Systems Manager Inventory",
  "Resources": {
    "BasicResourceDataSync": {
      "Type": "AWS::SSM::ResourceDataSync",
      "Properties": {
        "SyncName": "My-USEAST2-Resource-Data-Sync",
        "BucketName": "my-us-east-2-rds-bucket",
        "BucketRegion": "us-east-2",
        "SyncFormat": "JsonSerDe",
        "BucketPrefix": "rds"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ssm-resourcedatasync--examples--AWS_Systems_Manager_Resource_Data_Sync--yaml"></a>

```
---
Description: "Create a Resource Data Sync for Systems Manager Inventory"
Resources:
  BasicResourceDataSync:
    Type: "AWS::SSM::ResourceDataSync"
    Properties:
      SyncName: "My-USEAST2-Resource-Data-Sync"
      BucketName: "my-us-east-2-rds-bucket"
      BucketRegion: "us-east-2"
      SyncFormat: "JsonSerDe"
      BucketPrefix: "rds"
```

## See Also<a name="aws-resource-ssm-resourcedatasync--seealso"></a>
+  [What is Systems Manager?](https://docs.aws.amazon.com/systems-manager/latest/userguide/what-is-systems-manager.html) 
+  [AWS Systems Manager Inventory](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-inventory.html) 
+  [Configuring Inventory Collection](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-inventory-configuring.html) 

## Supported Regions

This ResourceType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `cn-north-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-gov-west-1`
- `us-west-1`
- `us-west-2`
