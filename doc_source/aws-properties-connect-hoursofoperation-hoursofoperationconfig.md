# AWS::Connect::HoursOfOperation HoursOfOperationConfig<a name="aws-properties-connect-hoursofoperation-hoursofoperationconfig"></a>

Contains information about the hours of operation\.

## Syntax<a name="aws-properties-connect-hoursofoperation-hoursofoperationconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-hoursofoperation-hoursofoperationconfig-syntax.json"></a>

```
{
  "[Day](#cfn-connect-hoursofoperation-hoursofoperationconfig-day)" : String,
  "[EndTime](#cfn-connect-hoursofoperation-hoursofoperationconfig-endtime)" : HoursOfOperationTimeSlice,
  "[StartTime](#cfn-connect-hoursofoperation-hoursofoperationconfig-starttime)" : HoursOfOperationTimeSlice
}
```

### YAML<a name="aws-properties-connect-hoursofoperation-hoursofoperationconfig-syntax.yaml"></a>

```
  [Day](#cfn-connect-hoursofoperation-hoursofoperationconfig-day): String
  [EndTime](#cfn-connect-hoursofoperation-hoursofoperationconfig-endtime): 
    HoursOfOperationTimeSlice
  [StartTime](#cfn-connect-hoursofoperation-hoursofoperationconfig-starttime): 
    HoursOfOperationTimeSlice
```

## Properties<a name="aws-properties-connect-hoursofoperation-hoursofoperationconfig-properties"></a>

`Day`  <a name="cfn-connect-hoursofoperation-hoursofoperationconfig-day"></a>
The day that the hours of operation applies to\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `FRIDAY | MONDAY | SATURDAY | SUNDAY | THURSDAY | TUESDAY | WEDNESDAY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndTime`  <a name="cfn-connect-hoursofoperation-hoursofoperationconfig-endtime"></a>
The end time that your contact center closes\.  
*Required*: Yes  
*Type*: [HoursOfOperationTimeSlice](aws-properties-connect-hoursofoperation-hoursofoperationtimeslice.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartTime`  <a name="cfn-connect-hoursofoperation-hoursofoperationconfig-starttime"></a>
The start time that your contact center opens\.  
*Required*: Yes  
*Type*: [HoursOfOperationTimeSlice](aws-properties-connect-hoursofoperation-hoursofoperationtimeslice.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)