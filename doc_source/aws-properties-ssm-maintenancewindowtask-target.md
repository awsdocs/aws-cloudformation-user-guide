# AWS Systems Manager MaintenanceWindowTask Target<a name="aws-properties-ssm-maintenancewindowtask-target"></a>

<a name="aws-properties-ssm-maintenancewindowtask-target-description"></a>The `Target` property type specifies targets \(either instances or tags\)\. You specify instances by using `Key=instanceids,Values=instanceid1,instanceid2`\. You specify tags by using `Key=tag name,Values=tag value` for a Maintenance Window task in AWS Systems Manager\.

<a name="aws-properties-ssm-maintenancewindowtask-target-inheritance"></a> `Target` is a property of the [AWS::SSM::MaintenanceWindowTask](aws-resource-ssm-maintenancewindowtask.md) resource\.

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
User\-defined criteria for sending commands that target instances that meet the criteria\. `Key` can be `tag:Amazon EC2 tag`or `InstanceIds`\. For more information about how to send commands that target instances by using `Key,Value` parameters, see [ Sending Commands to a Fleet](http://docs.aws.amazon.com/systems-manager/latest/userguide/send-commands-multiple.html) in the *AWS Systems Manager User Guide*\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Values`  <a name="cfn-ssm-maintenancewindowtask-target-values"></a>
User\-defined criteria that maps to `Key`\. For example, if you specify `tag:ServerRole`, you can specify `value:WebServer` to execute a command on instances that include Amazon EC2 tags of `ServerRole,WebServer`\. For more information about how to send commands that target instances using `Key,Value` parameters, see [ Sending Commands to a Fleet](http://docs.aws.amazon.com/systems-manager/latest/userguide/send-commands-multiple.html) in the *AWS Systems Manager User Guide*\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 