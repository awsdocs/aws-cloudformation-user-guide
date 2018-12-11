# AWS::WorkSpaces::Workspace<a name="aws-resource-workspaces-workspace"></a>

The `AWS::WorkSpaces::Workspace` resource creates an Amazon WorkSpaces workspace, which is a cloud\-based desktop experience for end users\. Before creating a Workspace in CloudFormation, you must register a Directory Service directory with Workspaces\. This process is documented at [Register a Directory with Amazon WorkSpaces](https://docs.aws.amazon.com/workspaces/latest/adminguide/register-deregister-directory.html)\. For more information, see the [https://docs.aws.amazon.com/workspaces/latest/adminguide/](https://docs.aws.amazon.com/workspaces/latest/adminguide/)\. 

**Topics**
+ [Syntax](#aws-resource-workspaces-workspace-syntax)
+ [Properties](#w4ab1c21c10d216c13b9)
+ [Return Values](#w4ab1c21c10d216c13c11)
+ [Example](#w4ab1c21c10d216c13c13)
+ [Amazon WorkSpaces Workspace WorkspaceProperties](aws-properties-workspaces-workspace-workspaceproperties.md)

## Syntax<a name="aws-resource-workspaces-workspace-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-workspaces-workspace-syntax.json"></a>

```
{
  "Type" : "AWS::WorkSpaces::Workspace",
  "Properties" : {
    "[BundleId](#cfn-workspaces-workspace-bundleid)" : String,
    "[DirectoryId](#cfn-workspaces-workspace-directoryid)" : String,
    "[RootVolumeEncryptionEnabled](#cfn-workspaces-workspace-rootvolumeencryptionenabled)" : Boolean,
    "[Tags](#cfn-workspaces-workspace-tags)" : [ [*Tag*](aws-properties-resource-tags.md), ... ],
    "[UserName](#cfn-workspaces-workspace-username)" : String,
    "[UserVolumeEncryptionEnabled](#cfn-workspaces-workspace-uservolumeencryptionenabled)" : Boolean,
    "[VolumeEncryptionKey](#cfn-workspaces-workspace-volumeencryptionkey)" : String,
    "[WorkspaceProperties](#cfn-workspaces-workspace-workspaceproperties)" : [*WorkspaceProperties*](aws-properties-workspaces-workspace-workspaceproperties.md)
  }
}
```

### YAML<a name="aws-resource-workspaces-workspace-syntax.yaml"></a>

```
Type: "AWS::WorkSpaces::Workspace"
Properties: 
  [BundleId](#cfn-workspaces-workspace-bundleid): String
  [DirectoryId](#cfn-workspaces-workspace-directoryid): String
  [RootVolumeEncryptionEnabled](#cfn-workspaces-workspace-rootvolumeencryptionenabled): Boolean
  [Tags](#cfn-workspaces-workspace-tags):
    - [*Tag*](aws-properties-resource-tags.md)
  [UserName](#cfn-workspaces-workspace-username): String
  [UserVolumeEncryptionEnabled](#cfn-workspaces-workspace-uservolumeencryptionenabled): Boolean
  [VolumeEncryptionKey](#cfn-workspaces-workspace-volumeencryptionkey): String
  [WorkspaceProperties](#cfn-workspaces-workspace-workspaceproperties)" : [*WorkspaceProperties*](aws-properties-workspaces-workspace-workspaceproperties.md)
```

## Properties<a name="w4ab1c21c10d216c13b9"></a>

`BundleId`  <a name="cfn-workspaces-workspace-bundleid"></a>
The identifier of the bundle from which you want to create the workspace\. A bundle specifies the details of the workspace, such as the installed applications and the size of CPU, memory, and storage\. Use the [DescribeWorkspaceBundles](https://docs.aws.amazon.com/workspaces/latest/devguide/API_DescribeWorkspaceBundles.html) action to list the bundles that AWS offers\.  
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.\. To update this property, you must also update another property that triggers a replacement, such as the `UserName` property\.

`DirectoryId`  <a name="cfn-workspaces-workspace-directoryid"></a>
The identifier of the AWS Directory Service directory in which you want to create the workspace\. The directory must already be registered with Amazon WorkSpaces\. Use the [DescribeWorkspaceDirectories](https://docs.aws.amazon.com/workspaces/latest/devguide/API_DescribeWorkspaceDirectories.html) action to list the directories that are available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RootVolumeEncryptionEnabled`  <a name="cfn-workspaces-workspace-rootvolumeencryptionenabled"></a>
Indicates whether Amazon WorkSpaces encrypts data stored on the root volume \(`C:` drive\)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: Updates are not supported\.\. To update this property, you must also update another property that triggers a replacement, such as the `UserName` property\.

`Tags`  <a name="cfn-workspaces-workspace-tags"></a>
The tags \(key\-value pairs\) for the WorkSpace\.  
 *Required*: No  
 *Type*: List of [Resource Tag](aws-properties-resource-tags.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`UserName`  <a name="cfn-workspaces-workspace-username"></a>
The name of the user to which the workspace is assigned\. This user name must exist in the specified AWS Directory Service directory\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`UserVolumeEncryptionEnabled`  <a name="cfn-workspaces-workspace-uservolumeencryptionenabled"></a>
Indicates whether Amazon WorkSpaces encrypts data stored on the user volume \(`D:` drive\)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: Updates are not supported\.\. To update this property, you must also update another property that triggers a replacement, such as the `UserName` property\.

`VolumeEncryptionKey`  <a name="cfn-workspaces-workspace-volumeencryptionkey"></a>
The AWS Key Management Service \(AWS KMS\) key ID that Amazon WorkSpaces uses to encrypt data stored on your workspace\.  
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.\. To update this property, you must also update another property that triggers a replacement, such as the `UserName` property\.

`WorkspaceProperties`  <a name="cfn-workspaces-workspace-workspaceproperties"></a>
The WorkSpace properties\.  
*Required*: No  
*Type*: [Amazon WorkSpaces Workspace WorkspaceProperties](aws-properties-workspaces-workspace-workspaceproperties.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w4ab1c21c10d216c13c11"></a>

### Ref<a name="w4ab1c21c10d216c13c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w4ab1c21c10d216c13c13"></a>

### <a name="w4ab1c21c10d216c13c13b2"></a>

The following example creates a workspace for user `test`\. The bundle and directory IDs are specified as parameters in the same template\.

#### JSON<a name="aws-resource-workspaces-workspace-example.json"></a>

```
"workspace1" : {
  "Type" : "AWS::WorkSpaces::Workspace",
  "Properties" : {
    "BundleId" : {"Ref" : "BundleId"},
    "DirectoryId" : {"Ref" : "DirectoryId"},
    "UserName" : "test"
  }
}
```

#### YAML<a name="aws-resource-workspaces-workspace-example.yaml"></a>

```
workspace1: 
  Type: "AWS::WorkSpaces::Workspace"
  Properties: 
    BundleId: 
      Ref: "BundleId"
    DirectoryId: 
      Ref: "DirectoryId"
    UserName: "test"
```