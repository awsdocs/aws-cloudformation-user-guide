# AWS::EC2::Instance HibernationOptions<a name="aws-properties-ec2-instance-hibernationoptions"></a>

Indicates whether your instance is configured for hibernation\. This parameter is valid only if the instance meets the [hibernation prerequisites](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Hibernate.html#hibernating-prerequisites)\. For more information, see [Hibernate Your Instance](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Hibernate.html) in the *Amazon Elastic Compute Cloud User Guide*\.

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
If this parameter is set to `true`, your instance is enabled for hibernation; otherwise, it is not enabled for hibernation\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)