# Amazon CloudWatch Events Rule RunCommandParameters<a name="aws-properties-events-rule-runcommandparameters"></a>

<a name="aws-properties-events-rule-runcommandparameters-description"></a>The `RunCommandParameters` property type specifies the parameters to use when an Amazon CloudWatch Events rule invokes the AWS Systems Manager Run Command\.

<a name="aws-properties-events-rule-runcommandparameters-inheritance"></a> `RunCommandParameters` is a property of the [CloudWatch Events Rule Target](aws-properties-events-rule-target.md) property type\. 

## Syntax<a name="aws-properties-events-rule-runcommandparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-rule-runcommandparameters-syntax.json"></a>

```
{
  "[RunCommandTargets](#cfn-events-rule-runcommandparameters-runcommandtargets)" : [ [*RunCommandTarget*](aws-properties-events-rule-runcommandtarget.md), ... ]
}
```

### YAML<a name="aws-properties-events-rule-runcommandparameters-syntax.yaml"></a>

```
[RunCommandTargets](#cfn-events-rule-runcommandparameters-runcommandtargets): 
  - [*RunCommandTarget*](aws-properties-events-rule-runcommandtarget.md)
```

## Properties<a name="aws-properties-events-rule-runcommandparameters-properties"></a>

For more information, including constraints and valid values, see [RunCommandParameters](http://docs.aws.amazon.com/AmazonCloudWatchEvents/latest/APIReference/API_RunCommandParameters.html) in the *Amazon CloudWatch Events API Reference*\.

`RunCommandTargets`  <a name="cfn-events-rule-runcommandparameters-runcommandtargets"></a>
The criteria \(either InstanceIds or a tag\) that specifies which EC2 instances the command is sent to\.  
Currently, you can include only one `RunCommandTarget` block, which specifies a list of InstanceIds or a tag\.
 *Required*: Yes  
 *Type*: List of [CloudWatch Events Rule RunCommandTarget](aws-properties-events-rule-runcommandtarget.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 