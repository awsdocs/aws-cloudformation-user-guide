# AWS::Lightsail::Instance Location<a name="aws-properties-lightsail-instance-location"></a>

`Location` is a property of the [AWS::Lightsail::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-instance.html) resource\. It describes the location for an instance\.

## Syntax<a name="aws-properties-lightsail-instance-location-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lightsail-instance-location-syntax.json"></a>

```
{
  "[AvailabilityZone](#cfn-lightsail-instance-location-availabilityzone)" : String,
  "[RegionName](#cfn-lightsail-instance-location-regionname)" : String
}
```

### YAML<a name="aws-properties-lightsail-instance-location-syntax.yaml"></a>

```
  [AvailabilityZone](#cfn-lightsail-instance-location-availabilityzone): String
  [RegionName](#cfn-lightsail-instance-location-regionname): String
```

## Properties<a name="aws-properties-lightsail-instance-location-properties"></a>

`AvailabilityZone`  <a name="cfn-lightsail-instance-location-availabilityzone"></a>
The Availability Zone for the instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegionName`  <a name="cfn-lightsail-instance-location-regionname"></a>
The name of the AWS Region for the instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)