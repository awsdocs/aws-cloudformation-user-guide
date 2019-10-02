# AWS::SSM::Association Target<a name="aws-properties-ssm-association-target"></a>

 `Target` is a property of the [AWS::SSM::Association](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-association.html) resource that specifies the targets for an SSM document in Systems Manager\. 

## Syntax<a name="aws-properties-ssm-association-target-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-association-target-syntax.json"></a>

```
{
  "[Key](#cfn-ssm-association-target-key)" : String,
  "[Values](#cfn-ssm-association-target-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-ssm-association-target-syntax.yaml"></a>

```
  [Key](#cfn-ssm-association-target-key): String
  [Values](#cfn-ssm-association-target-values): 
    - String
```

## Properties<a name="aws-properties-ssm-association-target-properties"></a>

`Key`  <a name="cfn-ssm-association-target-key"></a>
User\-defined criteria for sending commands that target instances that meet the criteria\. `Key` can be `tag:<Amazon EC2 tag>` or `InstanceIds`\. For more information about how to send commands that target instances using `Key,Value` parameters, see [Using Targets and Rate Controls to Send Commands to a Fleet](https://docs.aws.amazon.com/systems-manager/latest/userguide/send-commands-multiple.html#send-commands-targeting) in the *AWS Systems Manager User Guide*\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[\p{L}\p{Z}\p{N}_.:/=\-@]*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Values`  <a name="cfn-ssm-association-target-values"></a>
User\-defined criteria that maps to `Key`\. For example, if you specified `tag:ServerRole`, you could specify `value:WebServer` to run a command on instances that include Amazon EC2 tags of `ServerRole,WebServer`\. For more information about how to send commands that target instances using `Key,Value` parameters, see [Using Targets and Rate Controls to Send Commands to a Fleet](https://docs.aws.amazon.com/systems-manager/latest/userguide/send-commands-multiple.html) in the *AWS Systems Manager User Guide*\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Supported Regions

This PropertyType is supported by ***all*** regions.