# AWS::IoTAnalytics::Dataset OutputFileUriValue<a name="aws-properties-iotanalytics-dataset-outputfileurivalue"></a>

The value of the variable as a structure that specifies an output file URI\.

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
The URI of the location where dataset contents are stored, usually the URI of a file in an S3 bucket\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `[\w\.-]{1,255}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)