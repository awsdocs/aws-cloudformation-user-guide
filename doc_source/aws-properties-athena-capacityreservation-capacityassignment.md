# AWS::Athena::CapacityReservation CapacityAssignment<a name="aws-properties-athena-capacityreservation-capacityassignment"></a>

A mapping between one or more workgroups and a capacity reservation\.

## Syntax<a name="aws-properties-athena-capacityreservation-capacityassignment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-athena-capacityreservation-capacityassignment-syntax.json"></a>

```
{
  "[WorkgroupNames](#cfn-athena-capacityreservation-capacityassignment-workgroupnames)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-athena-capacityreservation-capacityassignment-syntax.yaml"></a>

```
  [WorkgroupNames](#cfn-athena-capacityreservation-capacityassignment-workgroupnames): 
    - String
```

## Properties<a name="aws-properties-athena-capacityreservation-capacityassignment-properties"></a>

`WorkgroupNames`  <a name="cfn-athena-capacityreservation-capacityassignment-workgroupnames"></a>
The list of workgroup names for the capacity assignment\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)