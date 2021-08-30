# AWS::IoTAnalytics::Pipeline Filter<a name="aws-properties-iotanalytics-pipeline-filter"></a>

An activity that filters a message based on its attributes\.

## Syntax<a name="aws-properties-iotanalytics-pipeline-filter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-pipeline-filter-syntax.json"></a>

```
{
  "[Filter](#cfn-iotanalytics-pipeline-filter-filter)" : String,
  "[Name](#cfn-iotanalytics-pipeline-filter-name)" : String,
  "[Next](#cfn-iotanalytics-pipeline-filter-next)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-pipeline-filter-syntax.yaml"></a>

```
  [Filter](#cfn-iotanalytics-pipeline-filter-filter): String
  [Name](#cfn-iotanalytics-pipeline-filter-name): String
  [Next](#cfn-iotanalytics-pipeline-filter-next): String
```

## Properties<a name="aws-properties-iotanalytics-pipeline-filter-properties"></a>

`Filter`  <a name="cfn-iotanalytics-pipeline-filter-filter"></a>
An expression that looks like an SQL WHERE clause that must return a Boolean value\.  
*Required*: No  
*Type*: [String](#aws-properties-iotanalytics-pipeline-filter)  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotanalytics-pipeline-filter-name"></a>
The name of the 'filter' activity\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Next`  <a name="cfn-iotanalytics-pipeline-filter-next"></a>
The next activity in the pipeline\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)