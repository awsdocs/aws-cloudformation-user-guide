# AWS IoT Analytics Dataset Action<a name="aws-properties-iotanalytics-dataset-action"></a>

<a name="aws-properties-iotanalytics-dataset-action-description"></a>The `Action` property type specifies a list of actions that create data set contents for an AWS IoT Analytics dataset\.

<a name="aws-properties-iotanalytics-dataset-action-inheritance"></a> `Action` is a property of the [AWS::IoTAnalytics::Dataset](aws-resource-iotanalytics-dataset.md) resource\.

## Syntax<a name="aws-properties-iotanalytics-dataset-action-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-action-syntax.json"></a>

```
{
  "[ActionName](#cfn-iotanalytics-dataset-action-actionname)" : String,
  "[ContainerAction](#cfn-iotanalytics-dataset-action-containeraction)" : [*ContainerAction*](aws-properties-iotanalytics-dataset-containeraction.md),
  "[QueryAction](#cfn-iotanalytics-dataset-action-queryaction)" : [*QueryAction*](aws-properties-iotanalytics-dataset-queryaction.md)
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-action-syntax.yaml"></a>

```
[ActionName](#cfn-iotanalytics-dataset-action-actionname): String
[ContainerAction](#cfn-iotanalytics-dataset-action-containeraction): 
  [*ContainerAction*](aws-properties-iotanalytics-dataset-containeraction.md)
[QueryAction](#cfn-iotanalytics-dataset-action-queryaction): 
  [*QueryAction*](aws-properties-iotanalytics-dataset-queryaction.md)
```

## Properties<a name="aws-properties-iotanalytics-dataset-action-properties"></a>

`ActionName`  <a name="cfn-iotanalytics-dataset-action-actionname"></a>
The name of the data set action\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ContainerAction`  <a name="cfn-iotanalytics-dataset-action-containeraction"></a>
Information which allows the system to run a containerized application in order to create the data set contents\. The application must be in a Docker container along with any needed support libraries\.  
 *Required*: No  
 *Type*: [*ContainerAction*](aws-properties-iotanalytics-dataset-containeraction.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`QueryAction`  <a name="cfn-iotanalytics-dataset-action-queryaction"></a>
Uses an SQL query to automatically create data set contents\.  
 *Required*: No  
 *Type*: [*QueryAction*](aws-properties-iotanalytics-dataset-queryaction.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-dataset-action-seealso"></a>
+ [CreateDataset](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-createdataset) in the *AWS IoT Analytics User Guide*