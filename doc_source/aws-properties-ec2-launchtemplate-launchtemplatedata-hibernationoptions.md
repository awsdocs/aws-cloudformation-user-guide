# AWS::EC2::LaunchTemplate HibernationOptions<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-hibernationoptions"></a>

Specifies whether your instance is configured for hibernation\. This parameter is valid only if the instance meets the [hibernation prerequisites](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Hibernate.html#hibernating-prerequisites)\. For more information, see [Hibernate Your Instance](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Hibernate.html) in the *Amazon Elastic Compute Cloud User Guide*\.

 `HibernationOptions` is a property of [AWS::EC2::LaunchTemplate LaunchTemplateData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata.html)\.

## Syntax<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-hibernationoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-hibernationoptions-syntax.json"></a>

```
{
  "[Configured](#cfn-ec2-launchtemplate-launchtemplatedata-hibernationoptions-configured)" : Boolean
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-hibernationoptions-syntax.yaml"></a>

```
  [Configured](#cfn-ec2-launchtemplate-launchtemplatedata-hibernationoptions-configured): Boolean
```

## Properties<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-hibernationoptions-properties"></a>

`Configured`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-hibernationoptions-configured"></a>
If you set this parameter to `true`, the instance is enabled for hibernation\.  
Default: `false`   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)