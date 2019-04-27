# AWS::EC2::CapacityReservation<a name="aws-resource-ec2-capacityreservation"></a>

The `AWS::EC2::CapacityReservation` resource specifies a new Capacity Reservation with the specified attributes\.

Capacity Reservation is an Amazon EC2 offering that lets you create and manage reserved Amazon EC2 capacity\. Capacity Reservations enable you to reserve capacity for your Amazon EC2 instances in a specific Availability Zone for any duration\. You can create a Capacity Reservation by choosing an Availability Zone and quantity \(number of instances\), along with other instance specifications, such as instance type and tenancy\. Once created, the Amazon EC2 capacity is held for you regardless of whether you run the instances or not\.

For more information, see [Capacity Reservations](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-capacity-reservations.html) in the *Amazon Elastic Compute Cloud User Guide*\.

## Syntax<a name="aws-resource-ec2-capacityreservation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-capacityreservation-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::CapacityReservation",
  "Properties" : {
    "[AvailabilityZone](#cfn-ec2-capacityreservation-availabilityzone)" : String,
    "[EbsOptimized](#cfn-ec2-capacityreservation-ebsoptimized)" : Boolean,
    "[EndDate](#cfn-ec2-capacityreservation-enddate)" : String,
    "[EndDateType](#cfn-ec2-capacityreservation-enddatetype)" : String,
    "[EphemeralStorage](#cfn-ec2-capacityreservation-ephemeralstorage)" : Boolean,
    "[InstanceCount](#cfn-ec2-capacityreservation-instancecount)" : Integer,
    "[InstanceMatchCriteria](#cfn-ec2-capacityreservation-instancematchcriteria)" : String,
    "[InstancePlatform](#cfn-ec2-capacityreservation-instanceplatform)" : String,
    "[InstanceType](#cfn-ec2-capacityreservation-instancetype)" : String,
    "[TagSpecifications](#cfn-ec2-capacityreservation-tagspecifications)" : [ [*TagSpecification*](aws-properties-ec2-capacityreservation-tagspecification.md), ... ],
    "[Tenancy](#cfn-ec2-capacityreservation-tenancy)" : String
  }
}
```

### YAML<a name="aws-resource-ec2-capacityreservation-syntax.yaml"></a>

```
Type: "AWS::EC2::CapacityReservation"
Properties:
  [AvailabilityZone](#cfn-ec2-capacityreservation-availabilityzone): String
  [EbsOptimized](#cfn-ec2-capacityreservation-ebsoptimized): Boolean
  [EndDate](#cfn-ec2-capacityreservation-enddate): String
  [EndDateType](#cfn-ec2-capacityreservation-enddatetype): String
  [EphemeralStorage](#cfn-ec2-capacityreservation-ephemeralstorage): Boolean
  [InstanceCount](#cfn-ec2-capacityreservation-instancecount): Integer
  [InstanceMatchCriteria](#cfn-ec2-capacityreservation-instancematchcriteria): String
  [InstancePlatform](#cfn-ec2-capacityreservation-instanceplatform): String
  [InstanceType](#cfn-ec2-capacityreservation-instancetype): String
  [TagSpecifications](#cfn-ec2-capacityreservation-tagspecifications): 
    - [*TagSpecification*](aws-properties-ec2-capacityreservation-tagspecification.md)
  [Tenancy](#cfn-ec2-capacityreservation-tenancy): String
```

## Properties<a name="aws-resource-ec2-capacityreservation-properties"></a>

`AvailabilityZone`  <a name="cfn-ec2-capacityreservation-availabilityzone"></a>
The Availability Zone in which to create the Capacity Reservation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`EbsOptimized`  <a name="cfn-ec2-capacityreservation-ebsoptimized"></a>
Indicates whether the Capacity Reservation supports EBS\-optimized instances\. This optimization provides dedicated throughput to Amazon EBS and an optimized configuration stack to provide optimal I/O performance\. This optimization isn't available with all instance types\. Additional usage charges apply when using an EBS\- optimized instance\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`EndDate`  <a name="cfn-ec2-capacityreservation-enddate"></a>
The date and time at which the Capacity Reservation expires\. When a Capacity Reservation expires, the reserved capacity is released and you can no longer launch instances into it\. The Capacity Reservation's state changes to `expired` when it reaches its end date and time\.  
You must provide an `EndDate` value if `EndDateType` is `limited`\. Omit `EndDate` if `EndDateType` is `unlimited`\.  
If the `EndDateType` is `limited`, the Capacity Reservation is cancelled within an hour from the specified time\. For example, if you specify `5/31/2019`, `13:30:55`, the Capacity Reservation is guaranteed to end between `13:30:55` and `14:30:55` on `5/31/2019`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EndDateType`  <a name="cfn-ec2-capacityreservation-enddatetype"></a>
Indicates the way in which the Capacity Reservation ends\. A Capacity Reservation can have one of the following end types:  
+ `unlimited` \- The Capacity Reservation remains active until you explicitly cancel it\. Do not provide an EndDate if the EndDateType is unlimited\.
+ `limited` \- The Capacity Reservation expires automatically at a specified date and time\. You must provide an EndDate value if the EndDateType value is limited\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EphemeralStorage`  <a name="cfn-ec2-capacityreservation-ephemeralstorage"></a>
Indicates whether the Capacity Reservation supports instances with temporary, block\-level storage\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`InstanceCount`  <a name="cfn-ec2-capacityreservation-instancecount"></a>
The number of instances for which to reserve capacity\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`InstanceMatchCriteria`  <a name="cfn-ec2-capacityreservation-instancematchcriteria"></a>
Indicates the type of instance launches that the Capacity Reservation accepts\. The options include:  
+ `open` \- The Capacity Reservation automatically matches all instances that have matching attributes \(instance type, platform, and Availability Zone\)\. Instances that have matching attributes run in the Capacity Reservation automatically without specifying any additional parameters\.
+ `targeted` \- The Capacity Reservation only accepts instances that have matching attributes \(instance type, platform, and Availability Zone\), and explicitly target the Capacity Reservation\. This ensures that only permitted instances can use the reserved capacity\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`InstancePlatform`  <a name="cfn-ec2-capacityreservation-instanceplatform"></a>
The type of operating system for which to reserve capacity\.  
Valid values include: `Linux/UNIX` \| `Red Hat Enterprise Linux` \| `SUSE Linux` \| `Windows` \| `Windows with SQL Server` \| `Windows with SQL Server Enterprise` \| `Windows with SQL Server Standard` \| `Windows with SQL Server Web`  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`InstanceType`  <a name="cfn-ec2-capacityreservation-instancetype"></a>
The instance type for which to reserve capacity\. For more information, see [Instance Types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`TagSpecifications`  <a name="cfn-ec2-capacityreservation-tagspecifications"></a>
The tags to apply to the Capacity Reservation at creation\.  
*Required*: No  
*Type*: List of [TagSpecification](aws-properties-ec2-capacityreservation-tagspecification.md) property types  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Tenancy`  <a name="cfn-ec2-capacityreservation-tenancy"></a>
Indicates the tenancy of the Capacity Reservation\. A Capacity Reservation can have one of the following tenancy settings:  
+ `default` \- The Capacity Reservation is created on hardware that is shared with other AWS accounts\.
+ `dedicated` \- The Capacity Reservation is created on single\-tenant hardware that is dedicated to a single AWS account\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="aws-resource-ec2-capacityreservation-returnvalues"></a>

### Ref<a name="aws-resource-ec2-capacityreservation-ref"></a>

When you pass the logical ID of an `AWS::EC2::CapacityReservation` resource to the intrinsic `Ref` function, the function returns the resource ID, such as `cr-1234ab5cd6789e0f1`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-resource-ec2-capacityreservation-getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`AvailabilityZone`  
Returns the Availability Zone in which the capacity is reserved\. For example: `us-east-1a`\.

`AvailableInstanceCount`  
Returns the remaining capacity, which indicates the number of instances that can be launched in the Capacity Reservation\. For example: `9`\.

`InstanceType`  
Returns the type of instance for which the capacity is reserved\. For example: `m4.large`\.

`Tenancy`  
Returns the tenancy of the Capacity Reservation\. For example: `dedicated`\.

`TotalInstanceCount`  
Returns the total number of instances for which the Capacity Reservation reserves capacity\. For example: `15`\.

For more information about using `Fn::GetAtt`, see [ Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Example<a name="aws-resource-ec2-capacityreservation-examples"></a>

The following example creates a Capacity Reservation that reserves capacity in the `us-east-1a` Availability Zone for `10` `m4.large` instances running a `linux/unix` operating system\.

### JSON<a name="aws-resource-ec2-capacityreservation-example1.json"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",
  "Resources" : {
    "MyCapacityReservation" : {
      "Type" : "AWS::EC2::CapacityReservation",
      "Properties" : {
        "AvailabilityZone" : "us-east-1a",
        "InstanceCount" : "10",
        "InstancePlatform" : "Linux/UNIX",
        "InstanceType" : "m4.large"
      }
    }
  }
}
```

### YAML<a name="aws-resource-ec2-capacityreservation-example1.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources:
  MyCapacityReservation:
    Type: AWS::EC2::CapacityReservation
    Properties: 
      AvailabilityZone: us-east-1a
      InstanceCount: 10
      InstancePlatform: Linux/UNIX
      InstanceType: m4.large
```

## See Also<a name="aws-resource-ec2-capacityreservation-seealso"></a>
+ [On\-Demand Capacity Reservations](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-capacity-reservations.html) in the *Amazon EC2 User Guide for Linux Instances*