# AWS::EC2::EC2Fleet OnDemandOptionsRequest<a name="aws-properties-ec2-ec2fleet-ondemandoptionsrequest"></a>

Specifies the allocation strategy of On\-Demand Instances in an EC2 Fleet\.

 `OnDemandOptionsRequest` is a property of the [AWS::EC2::EC2Fleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-ec2fleet.html) resource\.

## Syntax<a name="aws-properties-ec2-ec2fleet-ondemandoptionsrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-ec2fleet-ondemandoptionsrequest-syntax.json"></a>

```
{
  "[AllocationStrategy](#cfn-ec2-ec2fleet-ondemandoptionsrequest-allocationstrategy)" : String,
  "[CapacityReservationOptions](#cfn-ec2-ec2fleet-ondemandoptionsrequest-capacityreservationoptions)" : CapacityReservationOptionsRequest,
  "[MaxTotalPrice](#cfn-ec2-ec2fleet-ondemandoptionsrequest-maxtotalprice)" : String,
  "[MinTargetCapacity](#cfn-ec2-ec2fleet-ondemandoptionsrequest-mintargetcapacity)" : Integer,
  "[SingleAvailabilityZone](#cfn-ec2-ec2fleet-ondemandoptionsrequest-singleavailabilityzone)" : Boolean,
  "[SingleInstanceType](#cfn-ec2-ec2fleet-ondemandoptionsrequest-singleinstancetype)" : Boolean
}
```

### YAML<a name="aws-properties-ec2-ec2fleet-ondemandoptionsrequest-syntax.yaml"></a>

```
  [AllocationStrategy](#cfn-ec2-ec2fleet-ondemandoptionsrequest-allocationstrategy): String
  [CapacityReservationOptions](#cfn-ec2-ec2fleet-ondemandoptionsrequest-capacityreservationoptions): 
    CapacityReservationOptionsRequest
  [MaxTotalPrice](#cfn-ec2-ec2fleet-ondemandoptionsrequest-maxtotalprice): String
  [MinTargetCapacity](#cfn-ec2-ec2fleet-ondemandoptionsrequest-mintargetcapacity): Integer
  [SingleAvailabilityZone](#cfn-ec2-ec2fleet-ondemandoptionsrequest-singleavailabilityzone): Boolean
  [SingleInstanceType](#cfn-ec2-ec2fleet-ondemandoptionsrequest-singleinstancetype): Boolean
```

## Properties<a name="aws-properties-ec2-ec2fleet-ondemandoptionsrequest-properties"></a>

`AllocationStrategy`  <a name="cfn-ec2-ec2fleet-ondemandoptionsrequest-allocationstrategy"></a>
The order of the launch template overrides to use in fulfilling On\-Demand capacity\. If you specify `lowest-price`, EC2 Fleet uses price to determine the order, launching the lowest price first\. If you specify `prioritized`, EC2 Fleet uses the priority that you assigned to each launch template override, launching the highest priority first\. If you do not specify a value, EC2 Fleet defaults to `lowest-price`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `lowest-price | prioritized`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CapacityReservationOptions`  <a name="cfn-ec2-ec2fleet-ondemandoptionsrequest-capacityreservationoptions"></a>
The strategy for using unused Capacity Reservations for fulfilling On\-Demand capacity\. Supported only for fleets of type `instant`\.  
*Required*: No  
*Type*: [CapacityReservationOptionsRequest](aws-properties-ec2-ec2fleet-capacityreservationoptionsrequest.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaxTotalPrice`  <a name="cfn-ec2-ec2fleet-ondemandoptionsrequest-maxtotalprice"></a>
The maximum amount per hour for On\-Demand Instances that you're willing to pay\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MinTargetCapacity`  <a name="cfn-ec2-ec2fleet-ondemandoptionsrequest-mintargetcapacity"></a>
The minimum target capacity for On\-Demand Instances in the fleet\. If the minimum target capacity is not reached, the fleet launches no instances\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SingleAvailabilityZone`  <a name="cfn-ec2-ec2fleet-ondemandoptionsrequest-singleavailabilityzone"></a>
Indicates that the fleet launches all On\-Demand Instances into a single Availability Zone\. Supported only for fleets of type `instant`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SingleInstanceType`  <a name="cfn-ec2-ec2fleet-ondemandoptionsrequest-singleinstancetype"></a>
Indicates that the fleet uses a single instance type to launch all On\-Demand Instances in the fleet\. Supported only for fleets of type `instant`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-ec2-ec2fleet-ondemandoptionsrequest--seealso"></a>
+  [ OnDemandOptionsRequest](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_OnDemandOptionsRequest.html) in the *Amazon EC2 API Reference*