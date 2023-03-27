# AWS::M2::Environment HighAvailabilityConfig<a name="aws-properties-m2-environment-highavailabilityconfig"></a>

Defines the details of a high availability configuration\.

## Syntax<a name="aws-properties-m2-environment-highavailabilityconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-m2-environment-highavailabilityconfig-syntax.json"></a>

```
{
  "[DesiredCapacity](#cfn-m2-environment-highavailabilityconfig-desiredcapacity)" : Integer
}
```

### YAML<a name="aws-properties-m2-environment-highavailabilityconfig-syntax.yaml"></a>

```
  [DesiredCapacity](#cfn-m2-environment-highavailabilityconfig-desiredcapacity): Integer
```

## Properties<a name="aws-properties-m2-environment-highavailabilityconfig-properties"></a>

`DesiredCapacity`  <a name="cfn-m2-environment-highavailabilityconfig-desiredcapacity"></a>
The number of instances in a high availability configuration\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)