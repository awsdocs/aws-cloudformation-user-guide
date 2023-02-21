# AWS::IoT::JobTemplate JobExecutionsRetryConfig<a name="aws-properties-iot-jobtemplate-jobexecutionsretryconfig"></a>

The configuration that determines how many retries are allowed for each failure type for a job\.

## Syntax<a name="aws-properties-iot-jobtemplate-jobexecutionsretryconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-jobtemplate-jobexecutionsretryconfig-syntax.json"></a>

```
{
  "[RetryCriteriaList](#cfn-iot-jobtemplate-jobexecutionsretryconfig-retrycriterialist)" : [ RetryCriteria, ... ]
}
```

### YAML<a name="aws-properties-iot-jobtemplate-jobexecutionsretryconfig-syntax.yaml"></a>

```
  [RetryCriteriaList](#cfn-iot-jobtemplate-jobexecutionsretryconfig-retrycriterialist): 
    - RetryCriteria
```

## Properties<a name="aws-properties-iot-jobtemplate-jobexecutionsretryconfig-properties"></a>

`RetryCriteriaList`  <a name="cfn-iot-jobtemplate-jobexecutionsretryconfig-retrycriterialist"></a>
The list of criteria that determines how many retries are allowed for each failure type for a job\.  
*Required*: No  
*Type*: List of [RetryCriteria](aws-properties-iot-jobtemplate-retrycriteria.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)