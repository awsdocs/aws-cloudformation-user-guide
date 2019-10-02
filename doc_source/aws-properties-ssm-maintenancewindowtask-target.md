# AWS::SSM::MaintenanceWindowTask Target<a name="aws-properties-ssm-maintenancewindowtask-target"></a>

The `Target` property type specifies targets \(either instances or window target IDs\)\. You specify instances by using `Key=InstanceIds,Values=<instanceid1>,<instanceid2>`\. You specify window target IDs using `Key=WindowTargetIds,Values=<window-target-id-1>,<window-target-id-2>` for a maintenance window task in AWS Systems Manager\.

 `Target` is a property of the [AWS::SSM::MaintenanceWindowTask](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-maintenancewindowtask.html) property type\.

## Syntax<a name="aws-properties-ssm-maintenancewindowtask-target-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-maintenancewindowtask-target-syntax.json"></a>

```
{
  "[Key](#cfn-ssm-maintenancewindowtask-target-key)" : String,
  "[Values](#cfn-ssm-maintenancewindowtask-target-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-ssm-maintenancewindowtask-target-syntax.yaml"></a>

```
  [Key](#cfn-ssm-maintenancewindowtask-target-key): String
  [Values](#cfn-ssm-maintenancewindowtask-target-values): 
    - String
```

## Properties<a name="aws-properties-ssm-maintenancewindowtask-target-properties"></a>

`Key`  <a name="cfn-ssm-maintenancewindowtask-target-key"></a>
User\-defined criteria for sending commands that target instances that meet the criteria\. `Key` can be `InstanceIds` or `WindowTargetIds`\. For more information about how to target instances within a maintenance window task, see [About 'register\-task\-with\-maintenance\-window' Options and Values](https://docs.aws.amazon.com/systems-manager/latest/userguide/register-tasks-options.html) in the *AWS Systems Manager User Guide*\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[\p{L}\p{Z}\p{N}_.:/=\-@]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-ssm-maintenancewindowtask-target-values"></a>
User\-defined criteria that maps to `Key`\. For example, if you specify `InstanceIds`, you can specify `i-1234567890abcdef0,i-9876543210abcdef0` to run a command on two EC2 instances\. For more information about how to target instances within a maintenance window task, see [About 'register\-task\-with\-maintenance\-window' Options and Values](https://docs.aws.amazon.com/systems-manager/latest/userguide/register-tasks-options.html) in the *AWS Systems Manager User Guide*\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-ssm-maintenancewindowtask-target--seealso"></a>
+  [RegisterTargetWithMaintenanceWindow](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_RegisterTargetWithMaintenanceWindow.html) in the *AWS Systems Manager API Reference*\.

## Supported Regions

This PropertyType is supported by the following regions:

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
- `us-west-1`
- `us-west-2`
