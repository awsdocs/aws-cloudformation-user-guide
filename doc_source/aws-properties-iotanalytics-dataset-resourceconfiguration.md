# AWS IoT Analytics Dataset ResourceConfiguration<a name="aws-properties-iotanalytics-dataset-resourceconfiguration"></a>

<a name="aws-properties-iotanalytics-dataset-resourceconfiguration-description"></a>The `ResourceConfiguration` property type specifies the configuration of the resource which executes the 'containerAction' for an AWS IoT Analytics dataset\.

<a name="aws-properties-iotanalytics-dataset-resourceconfiguration-inheritance"></a> `ResourceConfiguration` is a property of the [ContainerAction](aws-properties-iotanalytics-dataset-containeraction.md) property type\.

## Syntax<a name="aws-properties-iotanalytics-dataset-resourceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-resourceconfiguration-syntax.json"></a>

```
{
  "[ComputeType](#cfn-iotanalytics-dataset-resourceconfiguration-computetype)" : String,
  "[VolumeSizeInGB](#cfn-iotanalytics-dataset-resourceconfiguration-volumesizeingb)" : Integer
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-resourceconfiguration-syntax.yaml"></a>

```
[ComputeType](#cfn-iotanalytics-dataset-resourceconfiguration-computetype): String
[VolumeSizeInGB](#cfn-iotanalytics-dataset-resourceconfiguration-volumesizeingb): Integer
```

## Properties<a name="aws-properties-iotanalytics-dataset-resourceconfiguration-properties"></a>

`ComputeType`  <a name="cfn-iotanalytics-dataset-resourceconfiguration-computetype"></a>
The type of the compute resource used to execute the 'containerAction' \(ACU\_1\|ACU\_2\)\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`VolumeSizeInGB`  <a name="cfn-iotanalytics-dataset-resourceconfiguration-volumesizeingb"></a>
The size of the persistent storage available to the resource instance used to execute the 'containerAction'\.  
 *Required*: Yes  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-dataset-resourceconfiguration-seealso"></a>
+ [CreateDataset](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-createdataset) in the *IoT Analytics User Guide*