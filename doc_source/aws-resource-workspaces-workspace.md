# AWS::WorkSpaces::Workspace<a name="aws-resource-workspaces-workspace"></a>

Specifies a WorkSpace\.

Updates are not supported for the `BundleId`, `RootVolumeEncryptionEnabled`, `UserVolumeEncryptionEnabled`, or `VolumeEncryptionKey` properties\. To update these properties, you must also update a property that triggers a replacement, such as the `UserName` property\.

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
      "[Tags](#cfn-workspaces-workspace-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[UserName](#cfn-workspaces-workspace-username)" : String,
      "[UserVolumeEncryptionEnabled](#cfn-workspaces-workspace-uservolumeencryptionenabled)" : Boolean,
      "[VolumeEncryptionKey](#cfn-workspaces-workspace-volumeencryptionkey)" : String,
      "[WorkspaceProperties](#cfn-workspaces-workspace-workspaceproperties)" : [WorkspaceProperties](aws-properties-workspaces-workspace-workspaceproperties.md)
    }
}
```

### YAML<a name="aws-resource-workspaces-workspace-syntax.yaml"></a>

```
Type: AWS::WorkSpaces::Workspace
Properties : 
﻿  [BundleId](#cfn-workspaces-workspace-bundleid) : String
﻿  [DirectoryId](#cfn-workspaces-workspace-directoryid) : String
﻿  [RootVolumeEncryptionEnabled](#cfn-workspaces-workspace-rootvolumeencryptionenabled) : Boolean
﻿  [Tags](#cfn-workspaces-workspace-tags) : 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
﻿  [UserName](#cfn-workspaces-workspace-username) : String
﻿  [UserVolumeEncryptionEnabled](#cfn-workspaces-workspace-uservolumeencryptionenabled) : Boolean
﻿  [VolumeEncryptionKey](#cfn-workspaces-workspace-volumeencryptionkey) : String
﻿  [WorkspaceProperties](#cfn-workspaces-workspace-workspaceproperties) : [WorkspaceProperties](aws-properties-workspaces-workspace-workspaceproperties.md)
```

## Properties<a name="aws-resource-workspaces-workspace-properties"></a>

`BundleId`  <a name="cfn-workspaces-workspace-bundleid"></a>
The identifier of the bundle for the WorkSpace\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^wsb-[0-9a-z]{8,63}$`

`DirectoryId`  <a name="cfn-workspaces-workspace-directoryid"></a>
The identifier of the AWS Directory Service directory for the WorkSpace\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^d-[0-9a-f]{8,63}$`

`RootVolumeEncryptionEnabled`  <a name="cfn-workspaces-workspace-rootvolumeencryptionenabled"></a>
Indicates whether the data stored on the root volume is encrypted\.  
*Required*: No  
*Type*: Boolean

`Tags`  <a name="cfn-workspaces-workspace-tags"></a>
The tags for the WorkSpace\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserName`  <a name="cfn-workspaces-workspace-username"></a>
The username of the user for the WorkSpace\. This username must exist in the AWS Directory Service directory for the WorkSpace\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `63`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UserVolumeEncryptionEnabled`  <a name="cfn-workspaces-workspace-uservolumeencryptionenabled"></a>
Indicates whether the data stored on the user volume is encrypted\.  
*Required*: No  
*Type*: Boolean

`VolumeEncryptionKey`  <a name="cfn-workspaces-workspace-volumeencryptionkey"></a>
The KMS key used to encrypt data stored on your WorkSpace\.  
*Required*: No  
*Type*: String

`WorkspaceProperties`  <a name="cfn-workspaces-workspace-workspaceproperties"></a>
The WorkSpace properties\.  
*Required*: No  
*Type*: [WorkspaceProperties](aws-properties-workspaces-workspace-workspaceproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-workspaces-workspace-return-values"></a>

### Ref<a name="aws-resource-workspaces-workspace-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See Also<a name="aws-resource-workspaces-workspace--seealso"></a>
+  [CreateWorkspaces](https://docs.aws.amazon.com/workspaces/latest/api/API_CreateWorkspaces.html) in the *Amazon WorkSpaces API Reference* 
+  [Launch a Virtual Desktop Using Amazon WorkSpaces](https://docs.aws.amazon.com/workspaces/latest/adminguide/launch-workspaces-tutorials.html) in the *Amazon WorkSpaces Administration Guide* 