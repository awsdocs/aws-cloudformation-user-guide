# AWS::FSx::DataRepositoryAssociation S3<a name="aws-properties-fsx-datarepositoryassociation-s3"></a>

The configuration for an Amazon S3 data repository linked to an Amazon FSx Lustre file system with a data repository association\. The configuration defines which file events \(new, changed, or deleted files or directories\) are automatically imported from the linked data repository to the file system or automatically exported from the file system to the data repository\.

## Syntax<a name="aws-properties-fsx-datarepositoryassociation-s3-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-datarepositoryassociation-s3-syntax.json"></a>

```
{
  "[AutoExportPolicy](#cfn-fsx-datarepositoryassociation-s3-autoexportpolicy)" : AutoExportPolicy,
  "[AutoImportPolicy](#cfn-fsx-datarepositoryassociation-s3-autoimportpolicy)" : AutoImportPolicy
}
```

### YAML<a name="aws-properties-fsx-datarepositoryassociation-s3-syntax.yaml"></a>

```
  [AutoExportPolicy](#cfn-fsx-datarepositoryassociation-s3-autoexportpolicy): 
    AutoExportPolicy
  [AutoImportPolicy](#cfn-fsx-datarepositoryassociation-s3-autoimportpolicy): 
    AutoImportPolicy
```

## Properties<a name="aws-properties-fsx-datarepositoryassociation-s3-properties"></a>

`AutoExportPolicy`  <a name="cfn-fsx-datarepositoryassociation-s3-autoexportpolicy"></a>
Describes a data repository association's automatic export policy\. The `AutoExportPolicy` defines the types of updated objects on the file system that will be automatically exported to the data repository\. As you create, modify, or delete files, Amazon FSx for Lustre automatically exports the defined changes asynchronously once your application finishes modifying the file\.  
This `AutoExportPolicy` is supported only for Amazon FSx for Lustre file systems with the `Persistent_2` deployment type\.  
*Required*: No  
*Type*: [AutoExportPolicy](aws-properties-fsx-datarepositoryassociation-autoexportpolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutoImportPolicy`  <a name="cfn-fsx-datarepositoryassociation-s3-autoimportpolicy"></a>
Describes the data repository association's automatic import policy\. The AutoImportPolicy defines how Amazon FSx keeps your file metadata and directory listings up to date by importing changes to your Amazon FSx for Lustre file system as you modify objects in a linked S3 bucket\.  
The `AutoImportPolicy` is supported only for Amazon FSx for Lustre file systems with the `Persistent_2` deployment type\.  
*Required*: No  
*Type*: [AutoImportPolicy](aws-properties-fsx-datarepositoryassociation-autoimportpolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)