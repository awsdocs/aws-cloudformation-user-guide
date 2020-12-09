# AWS::EC2::Instance CreditSpecification<a name="aws-properties-ec2-instance-creditspecification"></a>

Specifies the credit option for CPU usage of a T2, T3, or T3a instance\.

 `CreditSpecification` is a property of the [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) resource\.

## Syntax<a name="aws-properties-ec2-instance-creditspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-instance-creditspecification-syntax.json"></a>

```
{
  "[CPUCredits](#cfn-ec2-instance-creditspecification-cpucredits)" : String
}
```

### YAML<a name="aws-properties-ec2-instance-creditspecification-syntax.yaml"></a>

```
  [CPUCredits](#cfn-ec2-instance-creditspecification-cpucredits): String
```

## Properties<a name="aws-properties-ec2-instance-creditspecification-properties"></a>

`CPUCredits`  <a name="cfn-ec2-instance-creditspecification-cpucredits"></a>
The credit option for CPU usage of the instance\. Valid values are `standard` and `unlimited`\. `T3` instances launch as `unlimited` by default\. `T2` instances launch as `standard` by default\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)