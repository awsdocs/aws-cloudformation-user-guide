# AWS::IoTAnalytics::Pipeline RemoveAttributes<a name="aws-properties-iotanalytics-pipeline-removeattributes"></a>

An activity that removes attributes from a message\.

## Syntax<a name="aws-properties-iotanalytics-pipeline-removeattributes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-pipeline-removeattributes-syntax.json"></a>

```
{
  "[Attributes](#cfn-iotanalytics-pipeline-removeattributes-attributes)" : [ String, ... ],
  "[Name](#cfn-iotanalytics-pipeline-removeattributes-name)" : String,
  "[Next](#cfn-iotanalytics-pipeline-removeattributes-next)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-pipeline-removeattributes-syntax.yaml"></a>

```
  [Attributes](#cfn-iotanalytics-pipeline-removeattributes-attributes): 
    - String
  [Name](#cfn-iotanalytics-pipeline-removeattributes-name): String
  [Next](#cfn-iotanalytics-pipeline-removeattributes-next): String
```

## Properties<a name="aws-properties-iotanalytics-pipeline-removeattributes-properties"></a>

`Attributes`  <a name="cfn-iotanalytics-pipeline-removeattributes-attributes"></a>
A list of 1\-50 attributes to remove from the message\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotanalytics-pipeline-removeattributes-name"></a>
The name of the 'removeAttributes' activity\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Next`  <a name="cfn-iotanalytics-pipeline-removeattributes-next"></a>
The next activity in the pipeline\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)