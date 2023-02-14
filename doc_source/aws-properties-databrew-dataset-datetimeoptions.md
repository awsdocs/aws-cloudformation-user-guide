# AWS::DataBrew::Dataset DatetimeOptions<a name="aws-properties-databrew-dataset-datetimeoptions"></a>

Represents additional options for correct interpretation of datetime parameters used in the Amazon S3 path of a dataset\.

## Syntax<a name="aws-properties-databrew-dataset-datetimeoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-dataset-datetimeoptions-syntax.json"></a>

```
{
  "[Format](#cfn-databrew-dataset-datetimeoptions-format)" : String,
  "[LocaleCode](#cfn-databrew-dataset-datetimeoptions-localecode)" : String,
  "[TimezoneOffset](#cfn-databrew-dataset-datetimeoptions-timezoneoffset)" : String
}
```

### YAML<a name="aws-properties-databrew-dataset-datetimeoptions-syntax.yaml"></a>

```
  [Format](#cfn-databrew-dataset-datetimeoptions-format): String
  [LocaleCode](#cfn-databrew-dataset-datetimeoptions-localecode): String
  [TimezoneOffset](#cfn-databrew-dataset-datetimeoptions-timezoneoffset): String
```

## Properties<a name="aws-properties-databrew-dataset-datetimeoptions-properties"></a>

`Format`  <a name="cfn-databrew-dataset-datetimeoptions-format"></a>
Required option, that defines the datetime format used for a date parameter in the Amazon S3 path\. Should use only supported datetime specifiers and separation characters, all litera a\-z or A\-Z character should be escaped with single quotes\. E\.g\. "MM\.dd\.yyyy\-'at'\-HH:mm"\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LocaleCode`  <a name="cfn-databrew-dataset-datetimeoptions-localecode"></a>
Optional value for a non\-US locale code, needed for correct interpretation of some date formats\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimezoneOffset`  <a name="cfn-databrew-dataset-datetimeoptions-timezoneoffset"></a>
Optional value for a timezone offset of the datetime parameter value in the Amazon S3 path\. Shouldn't be used if Format for this parameter includes timezone fields\. If no offset specified, UTC is assumed\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)