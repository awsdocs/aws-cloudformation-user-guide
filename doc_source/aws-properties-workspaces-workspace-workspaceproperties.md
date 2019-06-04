# AWS::WorkSpaces::Workspace WorkspaceProperties<a name="aws-properties-workspaces-workspace-workspaceproperties"></a>

Information about a WorkSpace\.

## Syntax<a name="aws-properties-workspaces-workspace-workspaceproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-workspaces-workspace-workspaceproperties-syntax.json"></a>

```
{
  "[ComputeTypeName](#cfn-workspaces-workspace-workspaceproperties-computetypename)" : String,
  "[RootVolumeSizeGib](#cfn-workspaces-workspace-workspaceproperties-rootvolumesizegib)" : Integer,
  "[RunningMode](#cfn-workspaces-workspace-workspaceproperties-runningmode)" : String,
  "[RunningModeAutoStopTimeoutInMinutes](#cfn-workspaces-workspace-workspaceproperties-runningmodeautostoptimeoutinminutes)" : Integer,
  "[UserVolumeSizeGib](#cfn-workspaces-workspace-workspaceproperties-uservolumesizegib)" : Integer
}
```

### YAML<a name="aws-properties-workspaces-workspace-workspaceproperties-syntax.yaml"></a>

```
  [ComputeTypeName](#cfn-workspaces-workspace-workspaceproperties-computetypename): String
  [RootVolumeSizeGib](#cfn-workspaces-workspace-workspaceproperties-rootvolumesizegib): Integer
  [RunningMode](#cfn-workspaces-workspace-workspaceproperties-runningmode): String
  [RunningModeAutoStopTimeoutInMinutes](#cfn-workspaces-workspace-workspaceproperties-runningmodeautostoptimeoutinminutes): Integer
  [UserVolumeSizeGib](#cfn-workspaces-workspace-workspaceproperties-uservolumesizegib): Integer
```

## Properties<a name="aws-properties-workspaces-workspace-workspaceproperties-properties"></a>

`ComputeTypeName`  <a name="cfn-workspaces-workspace-workspaceproperties-computetypename"></a>
The compute type\. For more information, see [Amazon WorkSpaces Bundles](http://aws.amazon.com/workspaces/details/#Amazon_WorkSpaces_Bundles)\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `GRAPHICS | GRAPHICSPRO | PERFORMANCE | POWER | POWERPRO | STANDARD | VALUE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RootVolumeSizeGib`  <a name="cfn-workspaces-workspace-workspaceproperties-rootvolumesizegib"></a>
The size of the root volume\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RunningMode`  <a name="cfn-workspaces-workspace-workspaceproperties-runningmode"></a>
The running mode\. For more information, see [Manage the WorkSpace Running Mode](https://docs.aws.amazon.com/workspaces/latest/adminguide/running-mode.html)\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `ALWAYS_ON | AUTO_STOP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RunningModeAutoStopTimeoutInMinutes`  <a name="cfn-workspaces-workspace-workspaceproperties-runningmodeautostoptimeoutinminutes"></a>
The time after a user logs off when WorkSpaces are automatically stopped\. Configured in 60 minute intervals\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserVolumeSizeGib`  <a name="cfn-workspaces-workspace-workspaceproperties-uservolumesizegib"></a>
The size of the user storage\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-workspaces-workspace-workspaceproperties--seealso"></a>
+  [WorkspaceProperties](https://docs.aws.amazon.com/workspaces/latest/api/API_WorkspaceProperties.html) in the *Amazon WorkSpaces API Reference* 