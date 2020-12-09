# AWS::EC2::Instance HibernationOptions<a name="aws-properties-ec2-instance-hibernationoptions"></a>

Specifies the hibernation options for the instance\.

`HibernationOptions` is a property of the [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) resource\.

## Syntax<a name="aws-properties-ec2-instance-hibernationoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-instance-hibernationoptions-syntax.json"></a>

```
{
  "[Configured](#cfn-ec2-instance-hibernationoptions-configured)" : Boolean
}
```

### YAML<a name="aws-properties-ec2-instance-hibernationoptions-syntax.yaml"></a>

```
  [Configured](#cfn-ec2-instance-hibernationoptions-configured): Boolean
```

## Properties<a name="aws-properties-ec2-instance-hibernationoptions-properties"></a>

`Configured`  <a name="cfn-ec2-instance-hibernationoptions-configured"></a>
If you set this parameter to `true`, your instance is enabled for hibernation\.  
Default: `false`   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)