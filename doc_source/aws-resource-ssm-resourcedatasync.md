# AWS::SSM::ResourceDataSync<a name="aws-resource-ssm-resourcedatasync"></a>

The `AWS::SSM::ResourceDataSync` resource creates or deletes a Resource Data Sync for Systems Manager Inventory\. You can use Resource Data Sync to send Inventory data collected from all of your Systems Manager managed instances to a single Amazon S3 bucket that you have already created in your account\. Resource Data Sync then automatically updates the centralized data when new Inventory data is collected\. For more information, see [Configuring Resource Data Sync for Inventory](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-inventory-configuring.html#sysman-inventory-datasync) in the *AWS Systems Manager User Guide*\. 

**Topics**
+ [Syntax](#aws-resource-ssm-resourcedatasync-syntax)
+ [Properties](#aws-resource-ssm-resourcedatasync-properties)
+ [Return Values](#aws-resource-ssm-resourcedatasync-returnvalues)
+ [Examples](#aws-resource-ssm-resourcedatasync-examples)
+ [See Also](#aws-resource-ssm-resourcedatasync-seealso)

## Syntax<a name="aws-resource-ssm-resourcedatasync-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-resourcedatasync-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::ResourceDataSync",
  "Properties" : {
    "[KMSKeyArn](#cfn-ssm-resourcedatasync-kmskeyarn)" : String,
    "[BucketName](#cfn-ssm-resourcedatasync-bucketname)" : String,
    "[BucketRegion](#cfn-ssm-resourcedatasync-bucketregion)" : String,
    "[SyncFormat](#cfn-ssm-resourcedatasync-syncformat)" : String,
    "[SyncName](#cfn-ssm-resourcedatasync-syncname)" : String,
    "[BucketPrefix](#cfn-ssm-resourcedatasync-bucketprefix)" : String
  }
}
```

### YAML<a name="aws-resource-ssm-resourcedatasync-syntax.yaml"></a>

```
Type: "AWS::SSM::ResourceDataSync"
Properties:
  [KMSKeyArn](#cfn-ssm-resourcedatasync-kmskeyarn): String
  [BucketName](#cfn-ssm-resourcedatasync-bucketname): String
  [BucketRegion](#cfn-ssm-resourcedatasync-bucketregion): String
  [SyncFormat](#cfn-ssm-resourcedatasync-syncformat): String
  [SyncName](#cfn-ssm-resourcedatasync-syncname): String
  [BucketPrefix](#cfn-ssm-resourcedatasync-bucketprefix): String
```

## Properties<a name="aws-resource-ssm-resourcedatasync-properties"></a>

`KMSKeyArn`  <a name="cfn-ssm-resourcedatasync-kmskeyarn"></a>
The ARN of an encryption key for a destination in Amazon S3\. You can use a KMS key to encrypt inventory data in Amazon S3\. You must specify a key that exist in the same region as the destination Amazon S3 bucket\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`BucketName`  <a name="cfn-ssm-resourcedatasync-bucketname"></a>
The name of the Amazon S3 bucket where the aggregated data is stored\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`BucketRegion`  <a name="cfn-ssm-resourcedatasync-bucketregion"></a>
The AWS Region with the Amazon S3 bucket targeted by the Resource Data Sync\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`SyncFormat`  <a name="cfn-ssm-resourcedatasync-syncformat"></a>
The format in which Resource Data Sync output will be stored in Amazon S3\. The following format is currently supported: JsonSerDe  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`SyncName`  <a name="cfn-ssm-resourcedatasync-syncname"></a>
A name for the Resource Data Sync\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`BucketPrefix`  <a name="cfn-ssm-resourcedatasync-bucketprefix"></a>
An Amazon S3 prefix for the bucket\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-ssm-resourcedatasync-returnvalues"></a>

### Ref<a name="aws-resource-ssm-resourcedatasync-ref"></a>

When you pass the logical ID of an `AWS::SSM::ResourceDataSync` resource to the intrinsic `Ref` function, the function returns the name of the Resource Data Sync, such as `TestResourceDataSync`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-ssm-resourcedatasync-examples"></a>

### AWS Systems Manager Resource Data Sync<a name="w4ab1c21c10e1198c17b3"></a>

The following examples send Inventory data collected from all of your managed instances in the US East \(Ohio\) Region \(us\-east\-2\) to a single Amazon S3 bucket\. Resource Data Sync then automatically updates the centralized data when new Inventory data is collected\.

#### JSON<a name="aws-resource-ssm-resourcedatasync-example1.json"></a>

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

#### YAML<a name="aws-resource-ssm-resourcedatasync-example1.yaml"></a>

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

## See Also<a name="aws-resource-ssm-resourcedatasync-seealso"></a>
+ [What is Systems Manager?](https://docs.aws.amazon.com/systems-manager/latest/userguide/what-is-systems-manager.html)
+ [AWS Systems Manager Inventory Manager](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-inventory.html)
+ [Configuring Inventory Collection](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-inventory-configuring.html)