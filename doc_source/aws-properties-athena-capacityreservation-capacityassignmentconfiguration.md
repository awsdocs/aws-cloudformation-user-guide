# AWS::Athena::CapacityReservation CapacityAssignmentConfiguration<a name="aws-properties-athena-capacityreservation-capacityassignmentconfiguration"></a>

Assigns Athena workgroups \(and hence their queries\) to capacity reservations\. A capacity reservation can have only one capacity assignment configuration, but the capacity assignment configuration can be made up of multiple individual assignments\. Each assignment specifies how Athena queries can consume capacity from the capacity reservation that their workgroup is mapped to\.

## Syntax<a name="aws-properties-athena-capacityreservation-capacityassignmentconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-athena-capacityreservation-capacityassignmentconfiguration-syntax.json"></a>

```
{
  "[CapacityAssignments](#cfn-athena-capacityreservation-capacityassignmentconfiguration-capacityassignments)" : [ CapacityAssignment, ... ]
}
```

### YAML<a name="aws-properties-athena-capacityreservation-capacityassignmentconfiguration-syntax.yaml"></a>

```
  [CapacityAssignments](#cfn-athena-capacityreservation-capacityassignmentconfiguration-capacityassignments): 
    - CapacityAssignment
```

## Properties<a name="aws-properties-athena-capacityreservation-capacityassignmentconfiguration-properties"></a>

`CapacityAssignments`  <a name="cfn-athena-capacityreservation-capacityassignmentconfiguration-capacityassignments"></a>
The list of assignments that make up the capacity assignment configuration\.  
*Required*: Yes  
*Type*: List of [CapacityAssignment](aws-properties-athena-capacityreservation-capacityassignment.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)