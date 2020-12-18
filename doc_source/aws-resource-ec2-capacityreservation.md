# AWS::EC2::CapacityReservation<a name="aws-resource-ec2-capacityreservation"></a>

Creates a new Capacity Reservation with the specified attributes\. For more information, see [Capacity Reservations](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-capacity-reservations.html) in the *Amazon Elastic Compute Cloud User Guide*\.

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
      "[TagSpecifications](#cfn-ec2-capacityreservation-tagspecifications)" : [ TagSpecification, ... ],
      "[Tenancy](#cfn-ec2-capacityreservation-tenancy)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-capacityreservation-syntax.yaml"></a>

```
Type: AWS::EC2::CapacityReservation
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
    - TagSpecification
  [Tenancy](#cfn-ec2-capacityreservation-tenancy): String
```

## Properties<a name="aws-resource-ec2-capacityreservation-properties"></a>

`AvailabilityZone`  <a name="cfn-ec2-capacityreservation-availabilityzone"></a>
The Availability Zone in which to create the Capacity Reservation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EbsOptimized`  <a name="cfn-ec2-capacityreservation-ebsoptimized"></a>
Indicates whether the Capacity Reservation supports EBS\-optimized instances\. This optimization provides dedicated throughput to Amazon EBS and an optimized configuration stack to provide optimal I/O performance\. This optimization isn't available with all instance types\. Additional usage charges apply when using an EBS\- optimized instance\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EndDate`  <a name="cfn-ec2-capacityreservation-enddate"></a>
The date and time at which the Capacity Reservation expires\. When a Capacity Reservation expires, the reserved capacity is released and you can no longer launch instances into it\. The Capacity Reservation's state changes to `expired` when it reaches its end date and time\.  
You must provide an `EndDate` value if `EndDateType` is `limited`\. Omit `EndDate` if `EndDateType` is `unlimited`\.  
If the `EndDateType` is `limited`, the Capacity Reservation is cancelled within an hour from the specified time\. For example, if you specify 5/31/2019, 13:30:55, the Capacity Reservation is guaranteed to end between 13:30:55 and 14:30:55 on 5/31/2019\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndDateType`  <a name="cfn-ec2-capacityreservation-enddatetype"></a>
Indicates the way in which the Capacity Reservation ends\. A Capacity Reservation can have one of the following end types:  
+  `unlimited` \- The Capacity Reservation remains active until you explicitly cancel it\. Do not provide an `EndDate` if the `EndDateType` is `unlimited`\.
+  `limited` \- The Capacity Reservation expires automatically at a specified date and time\. You must provide an `EndDate` value if the `EndDateType` value is `limited`\.
*Required*: No  
*Type*: String  
*Allowed values*: `limited | unlimited`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EphemeralStorage`  <a name="cfn-ec2-capacityreservation-ephemeralstorage"></a>
Indicates whether the Capacity Reservation supports instances with temporary, block\-level storage\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceCount`  <a name="cfn-ec2-capacityreservation-instancecount"></a>
The number of instances for which to reserve capacity\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceMatchCriteria`  <a name="cfn-ec2-capacityreservation-instancematchcriteria"></a>
Indicates the type of instance launches that the Capacity Reservation accepts\. The options include:  
+  `open` \- The Capacity Reservation automatically matches all instances that have matching attributes \(instance type, platform, and Availability Zone\)\. Instances that have matching attributes run in the Capacity Reservation automatically without specifying any additional parameters\.
+  `targeted` \- The Capacity Reservation only accepts instances that have matching attributes \(instance type, platform, and Availability Zone\), and explicitly target the Capacity Reservation\. This ensures that only permitted instances can use the reserved capacity\. 
Default: `open`   
*Required*: No  
*Type*: String  
*Allowed values*: `open | targeted`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstancePlatform`  <a name="cfn-ec2-capacityreservation-instanceplatform"></a>
The type of operating system for which to reserve capacity\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Linux with SQL Server Enterprise | Linux with SQL Server Standard | Linux with SQL Server Web | Linux/UNIX | Red Hat Enterprise Linux | SUSE Linux | Windows | Windows with SQL Server | Windows with SQL Server Enterprise | Windows with SQL Server Standard | Windows with SQL Server Web`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceType`  <a name="cfn-ec2-capacityreservation-instancetype"></a>
The instance type for which to reserve capacity\. For more information, see [Instance types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html) in the *Amazon EC2 User Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TagSpecifications`  <a name="cfn-ec2-capacityreservation-tagspecifications"></a>
The tags to apply to the Capacity Reservation during launch\.  
*Required*: No  
*Type*: List of [TagSpecification](aws-properties-ec2-capacityreservation-tagspecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tenancy`  <a name="cfn-ec2-capacityreservation-tenancy"></a>
Indicates the tenancy of the Capacity Reservation\. A Capacity Reservation can have one of the following tenancy settings:  
+  `default` \- The Capacity Reservation is created on hardware that is shared with other AWS accounts\.
+  `dedicated` \- The Capacity Reservation is created on single\-tenant hardware that is dedicated to a single AWS account\.
*Required*: No  
*Type*: String  
*Allowed values*: `dedicated | default`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-capacityreservation-return-values"></a>

### Ref<a name="aws-resource-ec2-capacityreservation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ID, such as `cr-1234ab5cd6789e0f1`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-capacityreservation-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-capacityreservation-return-values-fn--getatt-fn--getatt"></a>

`AvailabilityZone`  <a name="AvailabilityZone-fn::getatt"></a>
Returns the Availability Zone in which the capacity is reserved\. For example: `us-east-1a`\.

`AvailableInstanceCount`  <a name="AvailableInstanceCount-fn::getatt"></a>
Returns the remaining capacity, which indicates the number of instances that can be launched in the Capacity Reservation\. For example: `9`\.

`InstanceType`  <a name="InstanceType-fn::getatt"></a>
Returns the type of instance for which the capacity is reserved\. For example: `m4.large`\.

`Tenancy`  <a name="Tenancy-fn::getatt"></a>
Returns the tenancy of the Capacity Reservation\. For example: `dedicated`\.

`TotalInstanceCount`  <a name="TotalInstanceCount-fn::getatt"></a>
Returns the total number of instances for which the Capacity Reservation reserves capacity\. For example: `15`\.

## See also<a name="aws-resource-ec2-capacityreservation--seealso"></a>
+  [ On\-Demand Capacity Reservations](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-capacity-reservations.html) in the *Amazon Elastic Compute Cloud User Guide for Linux Instances* 

