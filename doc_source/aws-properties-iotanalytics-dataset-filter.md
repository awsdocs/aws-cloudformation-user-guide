# AWS::IoTAnalytics::Dataset Filter<a name="aws-properties-iotanalytics-dataset-filter"></a>

Information which is used to filter message data, to segregate it according to the time frame in which it arrives\.

## Syntax<a name="aws-properties-iotanalytics-dataset-filter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-filter-syntax.json"></a>

```
{
  "[DeltaTime](#cfn-iotanalytics-dataset-filter-deltatime)" : DeltaTime
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-filter-syntax.yaml"></a>

```
  [DeltaTime](#cfn-iotanalytics-dataset-filter-deltatime): 
    DeltaTime
```

## Properties<a name="aws-properties-iotanalytics-dataset-filter-properties"></a>

`DeltaTime`  <a name="cfn-iotanalytics-dataset-filter-deltatime"></a>
Used to limit data to that which has arrived since the last execution of the action\.  
*Required*: No  
*Type*: [DeltaTime](aws-properties-iotanalytics-dataset-deltatime.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)