# AWS::SSM::MaintenanceWindowTarget<a name="aws-resource-ssm-maintenancewindowtarget"></a>

The `AWS::SSM::MaintenanceWindowTarget` resource registers a target with a maintenance window for AWS Systems Manager\. For more information, see [ RegisterTargetWithMaintenanceWindow](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_RegisterTargetWithMaintenanceWindow.html) in the *AWS Systems Manager API Reference*\.

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
Properties: 
  [Description](#cfn-ssm-maintenancewindowtarget-description): String
  [Name](#cfn-ssm-maintenancewindowtarget-name): String
  [OwnerInformation](#cfn-ssm-maintenancewindowtarget-ownerinformation): String
  [ResourceType](#cfn-ssm-maintenancewindowtarget-resourcetype): String
  [Targets](#cfn-ssm-maintenancewindowtarget-targets): 
    - [Targets](aws-properties-ssm-maintenancewindowtarget-targets.md)
  [WindowId](#cfn-ssm-maintenancewindowtarget-windowid): String
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
The name for the maintenance window target\.  
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9_\-.]{3,128}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OwnerInformation`  <a name="cfn-ssm-maintenancewindowtarget-ownerinformation"></a>
A user\-provided value that will be included in any CloudWatch events that are raised while running tasks for these targets in this maintenance window\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceType`  <a name="cfn-ssm-maintenancewindowtarget-resourcetype"></a>
The type of target that is being registered with the maintenance window\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `INSTANCE | RESOURCE_GROUP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Targets`  <a name="cfn-ssm-maintenancewindowtarget-targets"></a>
The targets to register with the maintenance window\. In other words, the instances to run commands on when the maintenance window runs\.  
You must specify targets by using the `WindowTargetIds` parameter\.  
*Required*: Yes  
*Type*: [List](aws-properties-ssm-maintenancewindowtarget-targets.md) of [Targets](aws-properties-ssm-maintenancewindowtarget-targets.md)  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WindowId`  <a name="cfn-ssm-maintenancewindowtarget-windowid"></a>
The ID of the maintenance window to register the target with\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `20`  
*Pattern*: `^mw-[0-9a-f]{17}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-ssm-maintenancewindowtarget-return-values"></a>

### Ref<a name="aws-resource-ssm-maintenancewindowtarget-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the maintenance window target ID, such as `12a345b6-bbb7-4bb6-90b0-8c9577a2d2b9`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ssm-maintenancewindowtarget--examples"></a>

### AWS Systems Manager Maintenance Window Target Example<a name="aws-resource-ssm-maintenancewindowtarget--examples--AWS_Systems_Manager_Maintenance_Window_Target_Example"></a>

The following example creates a Systems Manager maintenance window target that targets managed instances with the tag key `ENV` and the tag value `DEV`\.

#### JSON<a name="aws-resource-ssm-maintenancewindowtarget--examples--AWS_Systems_Manager_Maintenance_Window_Target_Example--json"></a>

```
{
    "Resources": {
        "MaintenanceWindowTarget": {
            "Type": "AWS::SSM::MaintenanceWindowTarget",
            "Properties": {
                "WindowId": "MaintenanceWindow",
                "ResourceType": "INSTANCE",
                "Targets": [
                    {
                        "Key": "tag:ENV",
                        "Values": [
                            "DEV"
                        ]
                    }
                ],
                "OwnerInformation": "SSM Step Function Demo",
                "Name": "SSMStepFunctionDemo",
                "Description": "A target for demonstrating maintenance windows and step functions"
            },
            "DependsOn": "MaintenanceWindow"
        }
    }
}
```

#### YAML<a name="aws-resource-ssm-maintenancewindowtarget--examples--AWS_Systems_Manager_Maintenance_Window_Target_Example--yaml"></a>

```
---
Resources:
  MaintenanceWindowTarget:
    Type: AWS::SSM::MaintenanceWindowTarget
    Properties:
      WindowId: MaintenanceWindow
      ResourceType: INSTANCE
      Targets:
      - Key: tag:ENV
        Values:
        - DEV
      OwnerInformation: SSM Step Function Demo
      Name: SSMStepFunctionDemo
      Description: A target for demonstrating maintenance windows and step functions
    DependsOn: MaintenanceWindow
```

## See Also<a name="aws-resource-ssm-maintenancewindowtarget--seealso"></a>
+  [AWS::SSM::MaintenanceWindow](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-maintenancewindow.html) 
+  [AWS::SSM::MaintenanceWindowTask](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-maintenancewindowtask.html) 
+  [RegisterTaskWithMaintenanceWindow](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_RegisterTaskWithMaintenanceWindow.html) in the *AWS Systems Manager API Reference*\.