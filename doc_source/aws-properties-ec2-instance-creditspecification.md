# Amazon EC2 Instance CreditSpecification<a name="aws-properties-ec2-instance-creditspecification"></a>

<a name="aws-properties-ec2-instance-creditspecification-description"></a>The `CreditSpecification` property type specifies the credit option for CPU usage of a T2 instance\.

<a name="aws-properties-ec2-instance-creditspecification-inheritance"></a> `CreditSpecification` is a property of the [AWS::EC2::Instance](aws-properties-ec2-instance.md) resource\.

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
The credit option for CPU usage of a T2 instance\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 