# AWS::EC2::LaunchTemplate IamInstanceProfile<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile"></a>

Specifies an IAM instance profile, which is a container for an IAM role for your instance\. You can use an IAM role to distribute your AWS credentials to your instances\.

If you are creating the launch template for use with an Amazon EC2 Auto Scaling group, you can specify either the name or the ARN of the instance profile, but not both\.

 `IamInstanceProfile` is a property of [AWS::EC2::LaunchTemplate LaunchTemplateData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata.html)\.

## Syntax<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile-syntax.json"></a>

```
{
  "[Arn](#cfn-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile-arn)" : String,
  "[Name](#cfn-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile-name)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile-syntax.yaml"></a>

```
  [Arn](#cfn-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile-arn): String
  [Name](#cfn-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile-name): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile-properties"></a>

`Arn`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile-arn"></a>
The Amazon Resource Name \(ARN\) of the instance profile\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile-name"></a>
The name of the instance profile\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-iaminstanceprofile--seealso"></a>
+  [ LaunchTemplateIamInstanceProfileSpecificationRequest](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplateIamInstanceProfileSpecificationRequest.html) in the *Amazon Elastic Compute Cloud API Reference* 

