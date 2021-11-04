# AWS::DataBrew::Job JobSample<a name="aws-properties-databrew-job-jobsample"></a>

A sample configuration for profile jobs only, which determines the number of rows on which the profile job is run\. If a `JobSample` value isn't provided, the default is used\. The default value is CUSTOM\_ROWS for the mode parameter and 20,000 for the size parameter\.

## Syntax<a name="aws-properties-databrew-job-jobsample-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-job-jobsample-syntax.json"></a>

```
{
  "[Mode](#cfn-databrew-job-jobsample-mode)" : String,
  "[Size](#cfn-databrew-job-jobsample-size)" : Integer
}
```

### YAML<a name="aws-properties-databrew-job-jobsample-syntax.yaml"></a>

```
  [Mode](#cfn-databrew-job-jobsample-mode): String
  [Size](#cfn-databrew-job-jobsample-size): Integer
```

## Properties<a name="aws-properties-databrew-job-jobsample-properties"></a>

`Mode`  <a name="cfn-databrew-job-jobsample-mode"></a>
A value that determines whether the profile job is run on the entire dataset or a specified number of rows\. This value must be one of the following:  
+ FULL\_DATASET \- The profile job is run on the entire dataset\.
+ CUSTOM\_ROWS \- The profile job is run on the number of rows specified in the `Size` parameter\.
*Required*: No  
*Type*: String  
*Allowed values*: `CUSTOM_ROWS | FULL_DATASET`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Size`  <a name="cfn-databrew-job-jobsample-size"></a>
The `Size` parameter is only required when the mode is CUSTOM\_ROWS\. The profile job is run on the specified number of rows\. The maximum value for size is Long\.MAX\_VALUE\.  
Long\.MAX\_VALUE = 9223372036854775807  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)