# Amazon EC2 LaunchTemplate CreditSpecification<a name="aws-properties-ec2-launchtemplate-creditspecification"></a>

<a name="aws-properties-ec2-launchtemplate-creditspecification-description"></a>The `CreditSpecification` property type specifies the credit option for CPU usage of a T2 instance for an Amazon EC2 launch template\.

<a name="aws-properties-ec2-launchtemplate-creditspecification-inheritance"></a> `CreditSpecification` is a property of the [Amazon EC2 LaunchTemplate LaunchTemplateData](aws-properties-ec2-launchtemplate-launchtemplatedata.md) property type\.

## Syntax<a name="aws-properties-ec2-launchtemplate-creditspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-creditspecification-syntax.json"></a>

```
{
  "[CpuCredits](#cfn-ec2-launchtemplate-creditspecification-cpucredits)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-creditspecification-syntax.yaml"></a>

```
[CpuCredits](#cfn-ec2-launchtemplate-creditspecification-cpucredits): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-creditspecification-properties"></a>

`CpuCredits`  <a name="cfn-ec2-launchtemplate-creditspecification-cpucredits"></a>
The credit option for CPU usage of a T2 instance\. Valid values include `standard` and `unlimited`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-launchtemplate-creditspecification-seealso"></a>
+ [CreditSpecificationRequest](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreditSpecificationRequest.html) in the *Amazon EC2 API Reference*