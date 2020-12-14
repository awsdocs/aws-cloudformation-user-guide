# AWS::Events::Rule RunCommandParameters<a name="aws-properties-events-rule-runcommandparameters"></a>

The `RunCommandParameters` property type specifies the parameters to use when a rule invokes the AWS Systems Manager Run Command\. 

 `RunCommandParameters` is a property of the [Target](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-events-rule-target.html) property type\.

This parameter contains the criteria \(either InstanceIds or a tag\) used to specify which EC2 instances are to be sent the command\. 

## Syntax<a name="aws-properties-events-rule-runcommandparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-rule-runcommandparameters-syntax.json"></a>

```
{
  "[RunCommandTargets](#cfn-events-rule-runcommandparameters-runcommandtargets)" : [ RunCommandTarget, ... ]
}
```

### YAML<a name="aws-properties-events-rule-runcommandparameters-syntax.yaml"></a>

```
  [RunCommandTargets](#cfn-events-rule-runcommandparameters-runcommandtargets): 
    - RunCommandTarget
```

## Properties<a name="aws-properties-events-rule-runcommandparameters-properties"></a>

`RunCommandTargets`  <a name="cfn-events-rule-runcommandparameters-runcommandtargets"></a>
The criteria \(either InstanceIds or a tag\) that specifies which EC2 instances the command is sent to\.   
Currently, you can include only one `RunCommandTarget` block, which specifies a list of InstanceIds or a tag\.
*Required*: Yes  
*Type*: List of [RunCommandTarget](aws-properties-events-rule-runcommandtarget.md)  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)