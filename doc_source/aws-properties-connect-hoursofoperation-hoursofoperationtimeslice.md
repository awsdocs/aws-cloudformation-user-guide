# AWS::Connect::HoursOfOperation HoursOfOperationTimeSlice<a name="aws-properties-connect-hoursofoperation-hoursofoperationtimeslice"></a>

The start time or end time for an hours of operation\.

## Syntax<a name="aws-properties-connect-hoursofoperation-hoursofoperationtimeslice-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-hoursofoperation-hoursofoperationtimeslice-syntax.json"></a>

```
{
  "[Hours](#cfn-connect-hoursofoperation-hoursofoperationtimeslice-hours)" : Integer,
  "[Minutes](#cfn-connect-hoursofoperation-hoursofoperationtimeslice-minutes)" : Integer
}
```

### YAML<a name="aws-properties-connect-hoursofoperation-hoursofoperationtimeslice-syntax.yaml"></a>

```
  [Hours](#cfn-connect-hoursofoperation-hoursofoperationtimeslice-hours): Integer
  [Minutes](#cfn-connect-hoursofoperation-hoursofoperationtimeslice-minutes): Integer
```

## Properties<a name="aws-properties-connect-hoursofoperation-hoursofoperationtimeslice-properties"></a>

`Hours`  <a name="cfn-connect-hoursofoperation-hoursofoperationtimeslice-hours"></a>
The hours\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `23`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Minutes`  <a name="cfn-connect-hoursofoperation-hoursofoperationtimeslice-minutes"></a>
The minutes\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `59`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)