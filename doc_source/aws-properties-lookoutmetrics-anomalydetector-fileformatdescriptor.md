# AWS::LookoutMetrics::AnomalyDetector FileFormatDescriptor<a name="aws-properties-lookoutmetrics-anomalydetector-fileformatdescriptor"></a>

Contains information about a source file's formatting\.

## Syntax<a name="aws-properties-lookoutmetrics-anomalydetector-fileformatdescriptor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lookoutmetrics-anomalydetector-fileformatdescriptor-syntax.json"></a>

```
{
  "[CsvFormatDescriptor](#cfn-lookoutmetrics-anomalydetector-fileformatdescriptor-csvformatdescriptor)" : CsvFormatDescriptor,
  "[JsonFormatDescriptor](#cfn-lookoutmetrics-anomalydetector-fileformatdescriptor-jsonformatdescriptor)" : JsonFormatDescriptor
}
```

### YAML<a name="aws-properties-lookoutmetrics-anomalydetector-fileformatdescriptor-syntax.yaml"></a>

```
  [CsvFormatDescriptor](#cfn-lookoutmetrics-anomalydetector-fileformatdescriptor-csvformatdescriptor): 
    CsvFormatDescriptor
  [JsonFormatDescriptor](#cfn-lookoutmetrics-anomalydetector-fileformatdescriptor-jsonformatdescriptor): 
    JsonFormatDescriptor
```

## Properties<a name="aws-properties-lookoutmetrics-anomalydetector-fileformatdescriptor-properties"></a>

`CsvFormatDescriptor`  <a name="cfn-lookoutmetrics-anomalydetector-fileformatdescriptor-csvformatdescriptor"></a>
Contains information about how a source CSV data file should be analyzed\.  
*Required*: No  
*Type*: [CsvFormatDescriptor](aws-properties-lookoutmetrics-anomalydetector-csvformatdescriptor.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JsonFormatDescriptor`  <a name="cfn-lookoutmetrics-anomalydetector-fileformatdescriptor-jsonformatdescriptor"></a>
Contains information about how a source JSON data file should be analyzed\.  
*Required*: No  
*Type*: [JsonFormatDescriptor](aws-properties-lookoutmetrics-anomalydetector-jsonformatdescriptor.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)