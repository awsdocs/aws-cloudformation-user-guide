# AWS::EC2::LaunchTemplate LicenseSpecification<a name="aws-properties-ec2-launchtemplate-licensespecification"></a>

Specifies a license configuration for an instance\.

`LicenseSpecification` is a property of [AWS::EC2::LaunchTemplate LaunchTemplateData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata.html)\.

## Syntax<a name="aws-properties-ec2-launchtemplate-licensespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-licensespecification-syntax.json"></a>

```
{
  "[LicenseConfigurationArn](#cfn-ec2-launchtemplate-licensespecification-licenseconfigurationarn)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-licensespecification-syntax.yaml"></a>

```
  [LicenseConfigurationArn](#cfn-ec2-launchtemplate-licensespecification-licenseconfigurationarn): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-licensespecification-properties"></a>

`LicenseConfigurationArn`  <a name="cfn-ec2-launchtemplate-licensespecification-licenseconfigurationarn"></a>
The Amazon Resource Name \(ARN\) of the license configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)