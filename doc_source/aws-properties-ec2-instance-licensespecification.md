# Amazon Elastic Compute Cloud Instance LicenseSpecification<a name="aws-properties-ec2-instance-licensespecification"></a>

<a name="aws-properties-ec2-instance-licensespecification-description"></a>The `LicenseSpecification` property type associates a license configuration with an instance\.

<a name="aws-properties-ec2-instance-licensespecification-inheritance"></a> `LicenseSpecification` is a property of the [AWS::EC2::Instance](aws-properties-ec2-instance.md) resource\.

## Syntax<a name="aws-properties-ec2-instance-licensespecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-instance-licensespecification-syntax.json"></a>

```
{
  "[LicenseConfigurationArn](#cfn-ec2-instance-licensespecification-licenseconfigurationarn)" : String
}
```

### YAML<a name="aws-properties-ec2-instance-licensespecification-syntax.yaml"></a>

```
[LicenseConfigurationArn](#cfn-ec2-instance-licensespecification-licenseconfigurationarn): String
```

## Properties<a name="aws-properties-ec2-instance-licensespecification-properties"></a>

`LicenseConfigurationArn`  <a name="cfn-ec2-instance-licensespecification-licenseconfigurationarn"></a>
The Amazon Resource Name \(ARN\) of license configuration to associate with the instance\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 