# AWS Systems Manager MaintenanceWindowTarget Targets<a name="aws-properties-ssm-maintenancewindowtarget-targets"></a>

<a name="aws-properties-ssm-maintenancewindowtarget-targets-description"></a>The `Targets` property type specifies adding a target to a Maintenance Window target in AWS Systems Manager\.

<a name="aws-properties-ssm-maintenancewindowtarget-targets-inheritance"></a> `Targets` is a property of the [AWS::SSM::MaintenanceWindowTarget](aws-resource-ssm-maintenancewindowtarget.md) resource\. 

## Syntax<a name="aws-properties-ssm-maintenancewindowtarget-targets-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-maintenancewindowtarget-targets-syntax.json"></a>

```
{
  "[Key](#cfn-ssm-maintenancewindowtarget-targets-key)" : String,
  "[Values](#cfn-ssm-maintenancewindowtarget-targets-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-ssm-maintenancewindowtarget-targets-syntax.yaml"></a>

```
[Key](#cfn-ssm-maintenancewindowtarget-targets-key): String
[Values](#cfn-ssm-maintenancewindowtarget-targets-values): 
  - String
```

## Properties<a name="aws-properties-ssm-maintenancewindowtarget-targets-properties"></a>

`Key`  <a name="cfn-ssm-maintenancewindowtarget-targets-key"></a>
User\-defined criteria for sending commands that target instances that meet the criteria\. `Key` can be `tag:Amazon EC2 tag` or `InstanceIds`\. For more information about how to send commands that target instances using `Key,Value` parameters, see [ Sending Commands to a Fleet](http://docs.aws.amazon.com/systems-manager/latest/userguide/send-commands-multiple.html) in the *AWS Systems Manager User Guide*\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Values`  <a name="cfn-ssm-maintenancewindowtarget-targets-values"></a>
User\-defined criteria that maps to `Key`\. For example, if you specify `tag:ServerRole`, you can specify `value:WebServer` to execute a command on instances that include the Amazon EC2 tags of `ServerRole,WebServer`\. For more information about how to send commands that target instances using `Key,Value` parameters, see [ Sending Commands to a Fleet](http://docs.aws.amazon.com/systems-manager/latest/userguide/send-commands-multiple.html) in the *AWS Systems Manager User Guide*\.  
 *Required*: No  
 *Type*: List of strings  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 