# AWS::SSM::MaintenanceWindowTarget<a name="aws-resource-ssm-maintenancewindowtarget"></a>

The `AWS::SSM::MaintenanceWindowTarget` resource registers a target with a Maintenance Window for AWS Systems Manager\. For more information, see [ RegisterTargetWithMaintenanceWindow](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_RegisterTargetWithMaintenanceWindow.html) in the *AWS Systems Manager API Reference*\.

## Syntax<a name="aws-resource-ssm-maintenancewindowtarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-maintenancewindowtarget-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::MaintenanceWindowTarget",
  "Properties" : {
      "[Description](#cfn-ssm-maintenancewindowtarget-description)" : String,
      "[Name](#cfn-ssm-maintenancewindowtarget-name)" : String,
      "[OwnerInformation](#cfn-ssm-maintenancewindowtarget-ownerinformation)" : String,
      "[ResourceType](#cfn-ssm-maintenancewindowtarget-resourcetype)" : String,
      "[Targets](#cfn-ssm-maintenancewindowtarget-targets)" : [ [Targets](aws-properties-ssm-maintenancewindowtarget-targets.md), ... ],
      "[WindowId](#cfn-ssm-maintenancewindowtarget-windowid)" : String
    }
}
```

### YAML<a name="aws-resource-ssm-maintenancewindowtarget-syntax.yaml"></a>

```
Type: AWS::SSM::MaintenanceWindowTarget
Properties : 
﻿  [Description](#cfn-ssm-maintenancewindowtarget-description) : String
﻿  [Name](#cfn-ssm-maintenancewindowtarget-name) : String
﻿  [OwnerInformation](#cfn-ssm-maintenancewindowtarget-ownerinformation) : String
﻿  [ResourceType](#cfn-ssm-maintenancewindowtarget-resourcetype) : String
﻿  [Targets](#cfn-ssm-maintenancewindowtarget-targets) : 
    - [Targets](aws-properties-ssm-maintenancewindowtarget-targets.md)
﻿  [WindowId](#cfn-ssm-maintenancewindowtarget-windowid) : String
```

## Properties<a name="aws-resource-ssm-maintenancewindowtarget-properties"></a>

`Description`  <a name="cfn-ssm-maintenancewindowtarget-description"></a>
A description for the target\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-ssm-maintenancewindowtarget-name"></a>
The target name\.  
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9_\-.]{3,128}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OwnerInformation`  <a name="cfn-ssm-maintenancewindowtarget-ownerinformation"></a>
A user\-provided value that will be included in any CloudWatch events that are raised while running tasks for these targets in this Maintenance Window\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceType`  <a name="cfn-ssm-maintenancewindowtarget-resourcetype"></a>
The type of target that is being registered with the Maintenance Window\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `INSTANCE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Targets`  <a name="cfn-ssm-maintenancewindowtarget-targets"></a>
The targets, either instances or tags\.  
Specify instances using the following format:  
 `Key=instanceids,Values=<instanceid1>,<instanceid2>`   
Tags are specified using the following format:  
 `Key=tag:<tag name>,Values=<tag value>`\.  
*Required*: Yes  
*Type*: [List](aws-properties-ssm-maintenancewindowtarget-targets.md) of [Targets](aws-properties-ssm-maintenancewindowtarget-targets.md)  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WindowId`  <a name="cfn-ssm-maintenancewindowtarget-windowid"></a>
The ID of the Maintenance Window to register the target with\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `20`  
*Pattern*: `^mw-[0-9a-f]{17}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-ssm-maintenancewindowtarget-return-values"></a>

### Ref<a name="aws-resource-ssm-maintenancewindowtarget-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Maintenance Window target ID, such as `12a345b6-bbb7-4bb6-90b0-8c9577a2d2b9`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See Also<a name="aws-resource-ssm-maintenancewindowtarget--seealso"></a>
+  [AWS::SSM::MaintenanceWindow](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-maintenancewindow.html) 
+  [AWS::SSM::MaintenanceWindowTask](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-maintenancewindowtask.html) 
+  [RegisterTaskWithMaintenanceWindow](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_RegisterTaskWithMaintenanceWindow.html) in the *AWS Systems Manager API Reference*\.
