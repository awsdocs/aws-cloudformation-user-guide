# AWS::SSM::MaintenanceWindowTask Target<a name="aws-properties-ssm-maintenancewindowtask-target"></a>

The `Target` property type specifies targets \(either instances or tags\)\. You specify instances by using `Key=instanceids,Values=instanceid1,instanceid2 `\. You specify tags by using `Key=tag name,Values=tag value `for a Maintenance Window task in AWS Systems Manager\.

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
﻿  [Key](#cfn-ssm-maintenancewindowtask-target-key) : String
﻿  [Values](#cfn-ssm-maintenancewindowtask-target-values) : 
    - String
```

## Properties<a name="aws-properties-ssm-maintenancewindowtask-target-properties"></a>

`Key`  <a name="cfn-ssm-maintenancewindowtask-target-key"></a>
User\-defined criteria for sending commands that target instances that meet the criteria\. `Key` can be `tag:Amazon EC2 tag ` or `InstanceIds`\. For more information about how to send commands that target instances by using `Key,Value` parameters, see [Using Targets and Rate Controls to Send Commands to a Fleet](https://docs.aws.amazon.com/systems-manager/latest/userguide/send-commands-multiple.html) in the *AWS Systems Manager User Guide*\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[\p{L}\p{Z}\p{N}_.:/=\-@]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-ssm-maintenancewindowtask-target-values"></a>
User\-defined criteria that maps to `Key`\. For example, if you specify `tag:ServerRole`, you can specify `value:WebServer` to execute a command on instances that include Amazon EC2 tags of `ServerRole,WebServer`\. For more information about how to send commands that target instances using `Key,Value` parameters, see [Using Targets and Rate Controls to Send Commands to a Fleet](https://docs.aws.amazon.com/systems-manager/latest/userguide/send-commands-multiple.html) in the *AWS Systems Manager User Guide*\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)