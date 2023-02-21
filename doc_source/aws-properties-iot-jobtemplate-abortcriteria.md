# AWS::IoT::JobTemplate AbortCriteria<a name="aws-properties-iot-jobtemplate-abortcriteria"></a>

The criteria that determine when and how a job abort takes place\.

## Syntax<a name="aws-properties-iot-jobtemplate-abortcriteria-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-jobtemplate-abortcriteria-syntax.json"></a>

```
{
  "[Action](#cfn-iot-jobtemplate-abortcriteria-action)" : String,
  "[FailureType](#cfn-iot-jobtemplate-abortcriteria-failuretype)" : String,
  "[MinNumberOfExecutedThings](#cfn-iot-jobtemplate-abortcriteria-minnumberofexecutedthings)" : Integer,
  "[ThresholdPercentage](#cfn-iot-jobtemplate-abortcriteria-thresholdpercentage)" : Double
}
```

### YAML<a name="aws-properties-iot-jobtemplate-abortcriteria-syntax.yaml"></a>

```
  [Action](#cfn-iot-jobtemplate-abortcriteria-action): String
  [FailureType](#cfn-iot-jobtemplate-abortcriteria-failuretype): String
  [MinNumberOfExecutedThings](#cfn-iot-jobtemplate-abortcriteria-minnumberofexecutedthings): Integer
  [ThresholdPercentage](#cfn-iot-jobtemplate-abortcriteria-thresholdpercentage): Double
```

## Properties<a name="aws-properties-iot-jobtemplate-abortcriteria-properties"></a>

`Action`  <a name="cfn-iot-jobtemplate-abortcriteria-action"></a>
The type of job action to take to initiate the job abort\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FailureType`  <a name="cfn-iot-jobtemplate-abortcriteria-failuretype"></a>
The type of job execution failures that can initiate a job abort\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MinNumberOfExecutedThings`  <a name="cfn-iot-jobtemplate-abortcriteria-minnumberofexecutedthings"></a>
The minimum number of things which must receive job execution notifications before the job can be aborted\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ThresholdPercentage`  <a name="cfn-iot-jobtemplate-abortcriteria-thresholdpercentage"></a>
The minimum percentage of job execution failures that must occur to initiate the job abort\.  
 AWS IoT Core supports up to two digits after the decimal \(for example, 10\.9 and 10\.99, but not 10\.999\)\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)