# AWS::Events::Rule RunCommandTarget<a name="aws-properties-events-rule-runcommandtarget"></a>

The `RunCommandTarget` property type specifies information about the Amazon EC2 instances that the Run Command is sent to\. A `RunCommandTarget` block can include only one key, but the key can specify multiple values\. 

 `RunCommandTarget` is a property of the [RunCommandParameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-events-rule-runcommandparameters.html) property type\.

Information about the EC2 instances that are to be sent the command, specified as key\-value pairs\. Each `RunCommandTarget` block can include only one key, but this key may specify multiple values\.

## Syntax<a name="aws-properties-events-rule-runcommandtarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-rule-runcommandtarget-syntax.json"></a>

```
{
  "[Key](#cfn-events-rule-runcommandtarget-key)" : String,
  "[Values](#cfn-events-rule-runcommandtarget-values)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-events-rule-runcommandtarget-syntax.yaml"></a>

```
  [Key](#cfn-events-rule-runcommandtarget-key): String
  [Values](#cfn-events-rule-runcommandtarget-values): 
    - String
```

## Properties<a name="aws-properties-events-rule-runcommandtarget-properties"></a>

`Key`  <a name="cfn-events-rule-runcommandtarget-key"></a>
Can be either `tag:` *tag\-key* or `InstanceIds`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[\p{L}\p{Z}\p{N}_.:/=+\-@]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-events-rule-runcommandtarget-values"></a>
If `Key` is `tag:` *tag\-key*, `Values` is a list of tag values\. If `Key` is `InstanceIds`, `Values` is a list of Amazon EC2 instance IDs\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)