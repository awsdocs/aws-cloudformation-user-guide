# AWS::SSM::MaintenanceWindowTarget Targets<a name="aws-properties-ssm-maintenancewindowtarget-targets"></a>

The `Targets` property type specifies adding a target to a maintenance window target in AWS Systems Manager\.

 `Targets` is a property of the [AWS::SSM::MaintenanceWindowTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-maintenancewindowtarget.html) resource\.

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
User\-defined criteria for sending commands that target instances that meet the criteria\. `Key` can be `tag:<Amazon EC2 tag>` or `InstanceIds`\. For more information about how to send commands that target instances using `Key,Value` parameters, see [Using Targets and Rate Controls to Send Commands to a Fleet](https://docs.aws.amazon.com/systems-manager/latest/userguide/send-commands-multiple.html#send-commands-targeting) in the *AWS Systems Manager User Guide*\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[\p{L}\p{Z}\p{N}_.:/=\-@]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-ssm-maintenancewindowtarget-targets-values"></a>
User\-defined criteria that maps to `Key`\. For example, if you specified `tag:ServerRole`, you could specify `value:WebServer` to run a command on instances that include Amazon EC2 tags of `ServerRole,WebServer`\. For more information about how to send commands that target instances using `Key,Value` parameters, see [Using Targets and Rate Controls to Send Commands to a Fleet](https://docs.aws.amazon.com/systems-manager/latest/userguide/send-commands-multiple.html) in the *AWS Systems Manager User Guide*\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-east-1`
- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `cn-north-1`
- `cn-northwest-1`
- `eu-central-1`
- `eu-north-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `me-south-1`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-gov-east-1`
- `us-gov-west-1`
- `us-west-1`
- `us-west-2`
