# AWS::EC2::CapacityReservationFleet<a name="aws-resource-ec2-capacityreservationfleet"></a>

Creates a new Capacity Reservation Fleet with the specified attributes\. For more information, see [Capacity Reservation Fleets](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/cr-fleets.html) in the *Amazon EC2 User Guide*\.

## Syntax<a name="aws-resource-ec2-capacityreservationfleet-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-capacityreservationfleet-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::CapacityReservationFleet",
  "Properties" : {
      "[AllocationStrategy](#cfn-ec2-capacityreservationfleet-allocationstrategy)" : String,
      "[EndDate](#cfn-ec2-capacityreservationfleet-enddate)" : String,
      "[InstanceMatchCriteria](#cfn-ec2-capacityreservationfleet-instancematchcriteria)" : String,
      "[InstanceTypeSpecifications](#cfn-ec2-capacityreservationfleet-instancetypespecifications)" : [ InstanceTypeSpecification, ... ],
      "[NoRemoveEndDate](#cfn-ec2-capacityreservationfleet-noremoveenddate)" : Boolean,
      "[RemoveEndDate](#cfn-ec2-capacityreservationfleet-removeenddate)" : Boolean,
      "[TagSpecifications](#cfn-ec2-capacityreservationfleet-tagspecifications)" : [ TagSpecification, ... ],
      "[Tenancy](#cfn-ec2-capacityreservationfleet-tenancy)" : String,
      "[TotalTargetCapacity](#cfn-ec2-capacityreservationfleet-totaltargetcapacity)" : Integer
    }
}
```

### YAML<a name="aws-resource-ec2-capacityreservationfleet-syntax.yaml"></a>

```
Type: AWS::EC2::CapacityReservationFleet
Properties: 
  [AllocationStrategy](#cfn-ec2-capacityreservationfleet-allocationstrategy): String
  [EndDate](#cfn-ec2-capacityreservationfleet-enddate): String
  [InstanceMatchCriteria](#cfn-ec2-capacityreservationfleet-instancematchcriteria): String
  [InstanceTypeSpecifications](#cfn-ec2-capacityreservationfleet-instancetypespecifications): 
    - InstanceTypeSpecification
  [NoRemoveEndDate](#cfn-ec2-capacityreservationfleet-noremoveenddate): Boolean
  [RemoveEndDate](#cfn-ec2-capacityreservationfleet-removeenddate): Boolean
  [TagSpecifications](#cfn-ec2-capacityreservationfleet-tagspecifications): 
    - TagSpecification
  [Tenancy](#cfn-ec2-capacityreservationfleet-tenancy): String
  [TotalTargetCapacity](#cfn-ec2-capacityreservationfleet-totaltargetcapacity): Integer
```

## Properties<a name="aws-resource-ec2-capacityreservationfleet-properties"></a>

`AllocationStrategy`  <a name="cfn-ec2-capacityreservationfleet-allocationstrategy"></a>
The strategy used by the Capacity Reservation Fleet to determine which of the specified instance types to use\. Currently, only the `prioritized` allocation strategy is supported\. For more information, see [ Allocation strategy](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/crfleet-concepts.html#allocation-strategy) in the Amazon EC2 User Guide\.  
Valid values: `prioritized`   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EndDate`  <a name="cfn-ec2-capacityreservationfleet-enddate"></a>
The date and time at which the Capacity Reservation Fleet expires\. When the Capacity Reservation Fleet expires, its state changes to `expired` and all of the Capacity Reservations in the Fleet expire\.  
The Capacity Reservation Fleet expires within an hour after the specified time\. For example, if you specify `5/31/2019`, `13:30:55`, the Capacity Reservation Fleet is guaranteed to expire between `13:30:55` and `14:30:55` on `5/31/2019`\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceMatchCriteria`  <a name="cfn-ec2-capacityreservationfleet-instancematchcriteria"></a>
Indicates the type of instance launches that the Capacity Reservation Fleet accepts\. All Capacity Reservations in the Fleet inherit this instance matching criteria\.  
Currently, Capacity Reservation Fleets support `open` instance matching criteria only\. This means that instances that have matching attributes \(instance type, platform, and Availability Zone\) run in the Capacity Reservations automatically\. Instances do not need to explicitly target a Capacity Reservation Fleet to use its reserved capacity\.  
*Required*: No  
*Type*: String  
*Allowed values*: `open`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceTypeSpecifications`  <a name="cfn-ec2-capacityreservationfleet-instancetypespecifications"></a>
Information about the instance types for which to reserve the capacity\.  
*Required*: No  
*Type*: List of [InstanceTypeSpecification](aws-properties-ec2-capacityreservationfleet-instancetypespecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NoRemoveEndDate`  <a name="cfn-ec2-capacityreservationfleet-noremoveenddate"></a>
Property description not available\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoveEndDate`  <a name="cfn-ec2-capacityreservationfleet-removeenddate"></a>
Property description not available\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TagSpecifications`  <a name="cfn-ec2-capacityreservationfleet-tagspecifications"></a>
The tags to assign to the Capacity Reservation Fleet\. The tags are automatically assigned to the Capacity Reservations in the Fleet\.  
*Required*: No  
*Type*: List of [TagSpecification](aws-properties-ec2-capacityreservationfleet-tagspecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tenancy`  <a name="cfn-ec2-capacityreservationfleet-tenancy"></a>
Indicates the tenancy of the Capacity Reservation Fleet\. All Capacity Reservations in the Fleet inherit this tenancy\. The Capacity Reservation Fleet can have one of the following tenancy settings:  
+  `default` \- The Capacity Reservation Fleet is created on hardware that is shared with other AWS accounts\.
+  `dedicated` \- The Capacity Reservations are created on single\-tenant hardware that is dedicated to a single AWS account\.
*Required*: No  
*Type*: String  
*Allowed values*: `default`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TotalTargetCapacity`  <a name="cfn-ec2-capacityreservationfleet-totaltargetcapacity"></a>
The total number of capacity units to be reserved by the Capacity Reservation Fleet\. This value, together with the instance type weights that you assign to each instance type used by the Fleet determine the number of instances for which the Fleet reserves capacity\. Both values are based on units that make sense for your workload\. For more information, see [ Total target capacity](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/crfleet-concepts.html#target-capacity) in the Amazon EC2 User Guide\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-capacityreservationfleet-return-values"></a>

### Ref<a name="aws-resource-ec2-capacityreservationfleet-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ID, such as `crf-abcdef01234567890`\.

### Fn::GetAtt<a name="aws-resource-ec2-capacityreservationfleet-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-capacityreservationfleet-return-values-fn--getatt-fn--getatt"></a>

`CapacityReservationFleetId`  <a name="CapacityReservationFleetId-fn::getatt"></a>
The ID of the Capacity Reservation Fleet\.

## Examples<a name="aws-resource-ec2-capacityreservationfleet--examples"></a>

### Creating a Capacity Reservation Fleet<a name="aws-resource-ec2-capacityreservationfleet--examples--Creating_a_Capacity_Reservation_Fleet"></a>

The following example creates a Capacity Feservation Fleet that creates Capacity Reservations for 2 `c4.large` or `c5.large` instances\. The Fleet prioritizes `c4.large` over `c5.large` and both instance types have the same weight\.

#### YAML<a name="aws-resource-ec2-capacityreservationfleet--examples--Creating_a_Capacity_Reservation_Fleet--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  EC2CapacityReservationFleetCanary:
    Type: 'AWS::EC2::CapacityReservationFleet'
    Properties:
      AllocationStrategy: "prioritized"
      InstanceTypeSpecifications:
        - InstanceType: "c4.large"
          InstancePlatform: "Linux/UNIX"
          AvailabilityZone: "us-east-1a"
          Weight: 1
          Priority: 1
        - InstanceType: "c5.large"
          InstancePlatform: "Linux/UNIX"
          AvailabilityZone: "us-east-1a"
          Weight: 1
          Priority: 2
      Tenancy: "default"
      TotalTargetCapacity: 2
      InstanceMatchCriteria: "open"
```