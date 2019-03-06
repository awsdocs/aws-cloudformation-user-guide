# AWS IoT Analytics Dataset ContainerAction<a name="aws-properties-iotanalytics-dataset-containeraction"></a>

<a name="aws-properties-iotanalytics-dataset-containeraction-description"></a>The `ContainerAction` property type specifies information which allows the system to run a containerized application in order to create the data set contents for an AWS IoT Analytics dataset\.

<a name="aws-properties-iotanalytics-dataset-containeraction-inheritance"></a> `ContainerAction` is a property of the [Action](aws-properties-iotanalytics-dataset-action.md) property type\.

## Syntax<a name="aws-properties-iotanalytics-dataset-containeraction-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-containeraction-syntax.json"></a>

```
{
  "[ExecutionRoleArn](#cfn-iotanalytics-dataset-containeraction-executionrolearn)" : String,
  "[Image](#cfn-iotanalytics-dataset-containeraction-image)" : String,
  "[ResourceConfiguration](#cfn-iotanalytics-dataset-containeraction-resourceconfiguration)" : [*ResourceConfiguration*](aws-properties-iotanalytics-dataset-resourceconfiguration.md),
  "[Variables](#cfn-iotanalytics-dataset-containeraction-variables)" : [ [*Variable*](aws-properties-iotanalytics-dataset-variable.md), ... ]
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-containeraction-syntax.yaml"></a>

```
[ExecutionRoleArn](#cfn-iotanalytics-dataset-containeraction-executionrolearn): String
[Image](#cfn-iotanalytics-dataset-containeraction-image): String
[ResourceConfiguration](#cfn-iotanalytics-dataset-containeraction-resourceconfiguration): 
  [*ResourceConfiguration*](aws-properties-iotanalytics-dataset-resourceconfiguration.md)
[Variables](#cfn-iotanalytics-dataset-containeraction-variables): 
  - [*Variable*](aws-properties-iotanalytics-dataset-variable.md)
```

## Properties<a name="aws-properties-iotanalytics-dataset-containeraction-properties"></a>

`ExecutionRoleArn`  <a name="cfn-iotanalytics-dataset-containeraction-executionrolearn"></a>
The ARN of the role which gives permission to the system to access needed resources in order to run the 'containerAction'\. This includes, at minimum, permission to retrieve the data set contents which are the input to the containerized application\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Image`  <a name="cfn-iotanalytics-dataset-containeraction-image"></a>
The ARN of the Docker container stored in your account\. The Docker container contains an application and needed support libraries and is used to generate data set contents\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ResourceConfiguration`  <a name="cfn-iotanalytics-dataset-containeraction-resourceconfiguration"></a>
Configuration of the resource that executes the 'containerAction'\.  
 *Required*: No  
 *Type*: List of [Variable](aws-properties-iotanalytics-dataset-variable.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Variables`  <a name="cfn-iotanalytics-dataset-containeraction-variables"></a>
The values of variables used within the context of the execution of the containerized application \(basically, parameters passed to the application\)\. Each variable must have a name and a value given by one of "stringValue", "datasetContentVersionValue", or "outputFileUriValue"\.  
 *Required*: No  
 *Type*: List of [Variable](aws-properties-iotanalytics-dataset-variable.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-dataset-containeraction-seealso"></a>
+ [ CreatePipeline](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-createpipeline) in the *AWS IoT Analytics User Guide*