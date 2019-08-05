# AWS::EC2::LaunchTemplate CapacityReservationSpecification<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-capacityreservationspecification"></a>

Specifies an instance's Capacity Reservation targeting option\. You can specify only one option at a time\.

 `CapacityReservationSpecification` is a property of the [ Amazon EC2 LaunchTemplate LaunchTemplateData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata.html) property type\.

## Syntax<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-capacityreservationspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-capacityreservationspecification-syntax.json"></a>

```
{
  "[CapacityReservationPreference](#cfn-ec2-launchtemplate-launchtemplatedata-capacityreservationspecification-capacityreservationpreference)" : [CapacityReservationPreference](aws-properties-ec2-launchtemplate-capacityreservationpreference.md),
  "[CapacityReservationTarget](#cfn-ec2-launchtemplate-launchtemplatedata-capacityreservationspecification-capacityreservationtarget)" : [CapacityReservationTarget](aws-properties-ec2-launchtemplate-capacityreservationtarget.md)
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-capacityreservationspecification-syntax.yaml"></a>

```
  [CapacityReservationPreference](#cfn-ec2-launchtemplate-launchtemplatedata-capacityreservationspecification-capacityreservationpreference):
    [CapacityReservationPreference](aws-properties-ec2-launchtemplate-capacityreservationpreference.md)
  [CapacityReservationTarget](#cfn-ec2-launchtemplate-launchtemplatedata-capacityreservationspecification-capacityreservationtarget):
    [CapacityReservationTarget](aws-properties-ec2-launchtemplate-capacityreservationtarget.md)
```

## Properties<a name="aws-properties-ec2-launchtemplate-launchtemplatedata-capacityreservationspecification-properties"></a>

`CapacityReservationPreference`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-capacityreservationspecification-capacityreservationpreference"></a>
Indicates the instance's Capacity Reservation preferences\. Possible preferences include:
+  `open` \- The instance can run in any `open` Capacity Reservation that has matching attributes \(instance type, platform, Availability Zone\)\.
+  `none` \- The instance avoids running in a Capacity Reservation even if one is available\. The instance runs in On\-Demand capacity\.
*Required*: No
*Type*: [CapacityReservationPreference](aws-properties-ec2-launchtemplate-capacityreservationpreference.md)
*Allowed Values*: `none | open`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CapacityReservationTarget`  <a name="cfn-ec2-launchtemplate-launchtemplatedata-capacityreservationspecification-capacityreservationtarget"></a>
Information about the target Capacity Reservation\.
*Required*: No
*Type*: [CapacityReservationTarget](aws-properties-ec2-launchtemplate-capacityreservationtarget.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
