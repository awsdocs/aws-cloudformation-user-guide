# AWS::IoT::JobTemplate AbortConfig<a name="aws-properties-iot-jobtemplate-abortconfig"></a>

The criteria that determine when and how a job abort takes place\.

## Syntax<a name="aws-properties-iot-jobtemplate-abortconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-jobtemplate-abortconfig-syntax.json"></a>

```
{
  "[CriteriaList](#cfn-iot-jobtemplate-abortconfig-criterialist)" : [ AbortCriteria, ... ]
}
```

### YAML<a name="aws-properties-iot-jobtemplate-abortconfig-syntax.yaml"></a>

```
  [CriteriaList](#cfn-iot-jobtemplate-abortconfig-criterialist): 
    - AbortCriteria
```

## Properties<a name="aws-properties-iot-jobtemplate-abortconfig-properties"></a>

`CriteriaList`  <a name="cfn-iot-jobtemplate-abortconfig-criterialist"></a>
The list of criteria that determine when and how to abort the job\.  
*Required*: Yes  
*Type*: List of [AbortCriteria](aws-properties-iot-jobtemplate-abortcriteria.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)