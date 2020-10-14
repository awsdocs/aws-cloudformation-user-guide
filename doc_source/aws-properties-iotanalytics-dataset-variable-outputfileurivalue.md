# AWS::IoTAnalytics::Dataset OutputFileUriValue<a name="aws-properties-iotanalytics-dataset-variable-outputfileurivalue"></a>

The value of the variable as a structure that specifies an output file URI\.

## Syntax<a name="aws-properties-iotanalytics-dataset-variable-outputfileurivalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-variable-outputfileurivalue-syntax.json"></a>

```
{
  "[FileName](#cfn-iotanalytics-dataset-variable-outputfileurivalue-filename)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-variable-outputfileurivalue-syntax.yaml"></a>

```
  [FileName](#cfn-iotanalytics-dataset-variable-outputfileurivalue-filename): String
```

## Properties<a name="aws-properties-iotanalytics-dataset-variable-outputfileurivalue-properties"></a>

`FileName`  <a name="cfn-iotanalytics-dataset-variable-outputfileurivalue-filename"></a>
The URI of the location where dataset contents are stored, usually the URI of a file in an S3 bucket\.  
*Required*: No  
*Type*: String  
*Pattern*: `[\w\.-]{1,255}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)