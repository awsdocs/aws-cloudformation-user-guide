# AWS::IoT::JobTemplate RetryCriteria<a name="aws-properties-iot-jobtemplate-retrycriteria"></a>

The criteria that determines how many retries are allowed for each failure type for a job\.

## Syntax<a name="aws-properties-iot-jobtemplate-retrycriteria-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-jobtemplate-retrycriteria-syntax.json"></a>

```
{
  "[FailureType](#cfn-iot-jobtemplate-retrycriteria-failuretype)" : String,
  "[NumberOfRetries](#cfn-iot-jobtemplate-retrycriteria-numberofretries)" : Integer
}
```

### YAML<a name="aws-properties-iot-jobtemplate-retrycriteria-syntax.yaml"></a>

```
  [FailureType](#cfn-iot-jobtemplate-retrycriteria-failuretype): String
  [NumberOfRetries](#cfn-iot-jobtemplate-retrycriteria-numberofretries): Integer
```

## Properties<a name="aws-properties-iot-jobtemplate-retrycriteria-properties"></a>

`FailureType`  <a name="cfn-iot-jobtemplate-retrycriteria-failuretype"></a>
The type of job execution failures that can initiate a job retry\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumberOfRetries`  <a name="cfn-iot-jobtemplate-retrycriteria-numberofretries"></a>
The number of retries allowed for a failure type for the job\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)