# AWS::SSM::Association Target<a name="aws-properties-ssm-association-target"></a>

 `Target` is a property of the [AWS::SSM::Association](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-association.html) resource that specifies the targets for an SSM document in Systems Manager\. You can target all instances in an AWS account by specifying the `InstanceIds` key with a value of `*`\. To view a JSON and a YAML example that targets all instances, see "Create an association for all managed instances in an AWS account" on the Examples page\.

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
User\-defined criteria for sending commands that target managed nodes that meet the criteria\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `163`  
*Pattern*: `^[\p{L}\p{Z}\p{N}_.:/=\-@]*$|resource-groups:ResourceTypeFilters|resource-groups:Name`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Values`  <a name="cfn-ssm-association-target-values"></a>
User\-defined criteria that maps to `Key`\. For example, if you specified `tag:ServerRole`, you could specify `value:WebServer` to run a command on instances that include EC2 tags of `ServerRole,WebServer`\.   
Depending on the type of target, the maximum number of values for a key might be lower than the global maximum of 50\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)