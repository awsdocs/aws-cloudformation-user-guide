# AWS::EC2::LaunchTemplate CreditSpecification<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-creditspecification"></a>

Specifies the credit option for CPU usage of a T2, T3, or T3a instance\.

 `CreditSpecification` is a property of [AWS::EC2::LaunchTemplate LaunchTemplateData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata.html)\.

## Syntax<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-creditspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-creditspecification-syntax.json"></a>

```
{
  "[CpuCredits](#cfn-ec2-launchtemplate-launchtemplatedata-creditspecification-cpucredits)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-creditspecification-syntax.yaml"></a>

```
  [CpuCredits](#cfn-ec2-launchtemplate-launchtemplatedata-creditspecification-cpucredits): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-creditspecification-properties"></a>

`CpuCredits`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-creditspecification-cpucredits"></a>
The credit option for CPU usage of a T2, T3, or T3a instance\. Valid values are `standard` and `unlimited`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-creditspecification--seealso"></a>
+  [ CreditSpecificationRequest](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreditSpecificationRequest.html) in the *Amazon Elastic Compute Cloud API Reference* 

