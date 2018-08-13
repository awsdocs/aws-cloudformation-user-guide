# Amazon EC2 LaunchTemplate IamInstanceProfile<a name="aws-properties-ec2-launchtemplate-iaminstanceprofile"></a>

<a name="aws-properties-ec2-launchtemplate-iaminstanceprofile-description"></a>The `IamInstanceProfile` property type specifies an IAM instance profile for an Amazon EC2 launch template\.

<a name="aws-properties-ec2-launchtemplate-iaminstanceprofile-inheritance"></a> `IamInstanceProfile` is a property of the [Amazon EC2 LaunchTemplate LaunchTemplateData](aws-properties-ec2-launchtemplate-launchtemplatedata.md) property type\.

## Syntax<a name="aws-properties-ec2-launchtemplate-iaminstanceprofile-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-iaminstanceprofile-syntax.json"></a>

```
{
  "[Arn](#cfn-ec2-launchtemplate-iaminstanceprofile-arn)" : String,
  "[Name](#cfn-ec2-launchtemplate-iaminstanceprofile-name)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-iaminstanceprofile-syntax.yaml"></a>

```
[Arn](#cfn-ec2-launchtemplate-iaminstanceprofile-arn): String
[Name](#cfn-ec2-launchtemplate-iaminstanceprofile-name): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-iaminstanceprofile-properties"></a>

`Arn`  <a name="cfn-ec2-launchtemplate-iaminstanceprofile-arn"></a>
The Amazon Resource Name \(ARN\) of the instance profile\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-ec2-launchtemplate-iaminstanceprofile-name"></a>
The name of the instance profile\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-launchtemplate-iaminstanceprofile-seealso"></a>
+ [LaunchTemplateIamInstanceProfileSpecificationRequest](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplateIamInstanceProfileSpecificationRequest.html.html) in the *Amazon EC2 API Reference*