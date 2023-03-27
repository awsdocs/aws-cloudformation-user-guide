# AWS::FSx::DataRepositoryAssociation AutoImportPolicy<a name="aws-properties-fsx-datarepositoryassociation-autoimportpolicy"></a>

Describes the data repository association's automatic import policy\. The AutoImportPolicy defines how Amazon FSx keeps your file metadata and directory listings up to date by importing changes to your Amazon FSx for Lustre file system as you modify objects in a linked S3 bucket\.

The `AutoImportPolicy` is supported only for Amazon FSx for Lustre file systems with the `Persistent_2` deployment type\.

## Syntax<a name="aws-properties-fsx-datarepositoryassociation-autoimportpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-datarepositoryassociation-autoimportpolicy-syntax.json"></a>

```
{
  "[Events](#cfn-fsx-datarepositoryassociation-autoimportpolicy-events)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-fsx-datarepositoryassociation-autoimportpolicy-syntax.yaml"></a>

```
  [Events](#cfn-fsx-datarepositoryassociation-autoimportpolicy-events): 
    - String
```

## Properties<a name="aws-properties-fsx-datarepositoryassociation-autoimportpolicy-properties"></a>

`Events`  <a name="cfn-fsx-datarepositoryassociation-autoimportpolicy-events"></a>
The `AutoImportPolicy` can have the following event values:  
+  `NEW` \- Amazon FSx automatically imports metadata of files added to the linked S3 bucket that do not currently exist in the FSx file system\.
+  `CHANGED` \- Amazon FSx automatically updates file metadata and invalidates existing file content on the file system as files change in the data repository\.
+  `DELETED` \- Amazon FSx automatically deletes files on the file system as corresponding files are deleted in the data repository\.
You can define any combination of event types for your `AutoImportPolicy`\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)