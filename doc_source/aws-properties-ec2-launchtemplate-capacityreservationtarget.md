# AWS::EC2::LaunchTemplate CapacityReservationTarget<a name="aws-properties-ec2-launchtemplate-capacityreservationtarget"></a>

Specifies a target Capacity Reservation\.

 `CapacityReservationTarget` is a property of the [ Amazon EC2 LaunchTemplate LaunchTemplateData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata.html) property type\.

## Syntax<a name="aws-properties-ec2-launchtemplate-capacityreservationtarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-capacityreservationtarget-syntax.json"></a>

```
{
  "[CapacityReservationId](#cfn-ec2-launchtemplate-capacityreservationtarget-capacityreservationid)" : String,
  "[CapacityReservationResourceGroupArn](#cfn-ec2-launchtemplate-capacityreservationtarget-capacityreservationresourcegrouparn)" : String
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-capacityreservationtarget-syntax.yaml"></a>

```
  [CapacityReservationId](#cfn-ec2-launchtemplate-capacityreservationtarget-capacityreservationid): String
  [CapacityReservationResourceGroupArn](#cfn-ec2-launchtemplate-capacityreservationtarget-capacityreservationresourcegrouparn): String
```

## Properties<a name="aws-properties-ec2-launchtemplate-capacityreservationtarget-properties"></a>

`CapacityReservationId`  <a name="cfn-ec2-launchtemplate-capacityreservationtarget-capacityreservationid"></a>
The ID of the Capacity Reservation in which to run the instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CapacityReservationResourceGroupArn`  <a name="cfn-ec2-launchtemplate-capacityreservationtarget-capacityreservationresourcegrouparn"></a>
The ARN of the Capacity Reservation resource group in which to run the instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)