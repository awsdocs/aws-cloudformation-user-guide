# AWS IoT Analytics Dataset OutputFileUriValue<a name="aws-properties-iotanalytics-dataset-outputfileurivalue"></a>

<a name="aws-properties-iotanalytics-dataset-outputfileurivalue-description"></a>The `OutputFileUriValue` property type specifies a variable value which contains an output file URI for an AWS IoT Analytics dataset\.

<a name="aws-properties-iotanalytics-dataset-outputfileurivalue-inheritance"></a> `OutputFileUriValue` is a property of the [Variable](aws-properties-iotanalytics-dataset-variable.md) property type\.

## Syntax<a name="aws-properties-iotanalytics-dataset-outputfileurivalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-outputfileurivalue-syntax.json"></a>

```
{
  "[FileName](#cfn-iotanalytics-dataset-outputfileurivalue-filename)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-outputfileurivalue-syntax.yaml"></a>

```
[FileName](#cfn-iotanalytics-dataset-outputfileurivalue-filename): String
```

## Properties<a name="aws-properties-iotanalytics-dataset-outputfileurivalue-properties"></a>

`FileName`  <a name="cfn-iotanalytics-dataset-outputfileurivalue-filename"></a>
The URI of the location where data set contents are stored, usually the URI of a file in an S3 bucket\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-iotanalytics-dataset-outputfileurivalue-seealso"></a>
+ [CreateDataset](https://docs.aws.amazon.com/iotanalytics/latest/userguide/api.html#cli-iotanalytics-createdataset) in the *AWS IoT Analytics User Guide*