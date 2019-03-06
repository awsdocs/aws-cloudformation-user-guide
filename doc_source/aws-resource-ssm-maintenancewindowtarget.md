# AWS::SSM::MaintenanceWindowTarget<a name="aws-resource-ssm-maintenancewindowtarget"></a>

The `AWS::SSM::MaintenanceWindowTarget` resource registers a target with a Maintenance Window for AWS Systems Manager\. For more information, see [ RegisterTargetWithMaintenanceWindow](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_RegisterTargetWithMaintenanceWindow.html) in the *AWS Systems Manager API Reference*\.

## Syntax<a name="aws-resource-ssm-maintenancewindowtarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-maintenancewindowtarget-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::MaintenanceWindowTarget",
  "Properties" : {
    "[OwnerInformation](#cfn-ssm-maintenancewindowtarget-ownerinformation)" : String,
    "[Description](#cfn-ssm-maintenancewindowtarget-description)" : String,
    "[WindowId](#cfn-ssm-maintenancewindowtarget-windowid)" : String,
    "[ResourceType](#cfn-ssm-maintenancewindowtarget-resourcetype)" : String,
    "[Targets](#cfn-ssm-maintenancewindowtarget-targets)" : [ [*Targets*](aws-properties-ssm-maintenancewindowtarget-targets.md), ... ],
    "[Name](#cfn-ssm-maintenancewindowtarget-name)" : String
  }
}
```

### YAML<a name="aws-resource-ssm-maintenancewindowtarget-syntax.yaml"></a>

```
Type: "AWS::SSM::MaintenanceWindowTarget"
Properties:
  [OwnerInformation](#cfn-ssm-maintenancewindowtarget-ownerinformation): String
  [Description](#cfn-ssm-maintenancewindowtarget-description): String
  [WindowId](#cfn-ssm-maintenancewindowtarget-windowid): String
  [ResourceType](#cfn-ssm-maintenancewindowtarget-resourcetype): String
  [Targets](#cfn-ssm-maintenancewindowtarget-targets): 
    - [*Targets*](aws-properties-ssm-maintenancewindowtarget-targets.md)
  [Name](#cfn-ssm-maintenancewindowtarget-name): String
```

## Properties<a name="aws-resource-ssm-maintenancewindowtarget-properties"></a>

`OwnerInformation`  <a name="cfn-ssm-maintenancewindowtarget-ownerinformation"></a>
A user\-provided value to include in any events in CloudWatch Events that are raised while running tasks for these targets in this Maintenance Window\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Description`  <a name="cfn-ssm-maintenancewindowtarget-description"></a>
A description for the target\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`WindowId`  <a name="cfn-ssm-maintenancewindowtarget-windowid"></a>
The ID of the Maintenance Window to register the target with\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ResourceType`  <a name="cfn-ssm-maintenancewindowtarget-resourcetype"></a>
The type of target that's being registered with the Maintenance Window\.  
 *Required*: Yes  
 *Type*: String  
*Valid values*: `INSTANCE`  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Targets`  <a name="cfn-ssm-maintenancewindowtarget-targets"></a>
The targets, either instances or tags\.  
Specify instances using the following format:  
 `Key=InstanceIds,Values=instance-id-1,instance-id-2`  
Specify tags using either of the following formats:  
 `Key=tag:tag-key,Values=tag-value-1,tag-value-2`  
`Key=tag-key,Values=tag-key-1,tag-key-2`  
 *Required*: Yes  
 *Type*: List of [Targets](aws-properties-ssm-maintenancewindowtarget-targets.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-ssm-maintenancewindowtarget-name"></a>
An optional name for the target\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-ssm-maintenancewindowtarget-returnvalues"></a>

### Ref<a name="w13ab1c21c10d231c22b9b3"></a>

When you pass the logical ID of an `AWS::SSM::MaintenanceWindowTarget` resource to the intrinsic `Ref` function, the function returns the maintenance window target ID, such as `12a345b6-bbb7-4bb6-90b0-8c9577a2d2b9`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## See Also<a name="aws-resource-ssm-maintenancewindowtarget-seealso"></a>
+ [AWS::SSM::MaintenanceWindow](aws-resource-ssm-maintenancewindow.md)
+ [AWS::SSM::MaintenanceWindowTask](aws-resource-ssm-maintenancewindowtask.md)
+ [ RegisterTargetWithMaintenanceWindow](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_RegisterTargetWithMaintenanceWindow.html) in the *AWS Systems Manager API Reference*