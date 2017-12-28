# Amazon CloudWatch Events Rule RunCommandTarget<a name="aws-properties-events-rule-runcommandtarget"></a>

<a name="aws-properties-events-rule-runcommandtarget-description"></a>The `RunCommandTarget` property type specifies information about the Amazon EC2 instances that the Run Command is sent to\. A `RunCommandTarget` block can include only one key, but the key can specify multiple values\.

<a name="aws-properties-events-rule-runcommandtarget-inheritance"></a> The `RunCommandTargets` property of the [CloudWatch Events Rule RunCommandParameters](aws-properties-events-rule-runcommandparameters.md) property type contains a list of `RunCommandTarget` property types\. 

## Syntax<a name="aws-properties-events-rule-runcommandtarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-rule-runcommandtarget-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-runcommandtarget-key)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-runcommandtarget-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-events-rule-runcommandtarget-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-runcommandtarget-key): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-events-rule-runcommandtarget-values): 
  - String
```

## Properties<a name="aws-properties-events-rule-runcommandtarget-properties"></a>

For more information, including constraints, see [RunCommandTarget](http://docs.aws.amazon.com/AmazonCloudWatchEvents/latest/APIReference/API_RunCommandTarget.html) in the *Amazon CloudWatch Events API Reference*\.

`Key`  
The key, either `tag: tag-key` or `InstanceIds`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`Values`  
A list of tag values or EC2 instance IDs\.  
 *Required*: Yes  
 *Type*: List of String values  
 *Update requires*: No interruption 