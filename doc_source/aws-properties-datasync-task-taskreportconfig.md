# AWS::DataSync::Task TaskReportConfig<a name="aws-properties-datasync-task-taskreportconfig"></a>

Specifies how you want to configure a task report, which provides detailed information about for your AWS DataSync transfer\.

For more information, see [Task reports](https://docs.aws.amazon.com/datasync/latest/userguide/creating-task-reports.html)\.

## Syntax<a name="aws-properties-datasync-task-taskreportconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datasync-task-taskreportconfig-syntax.json"></a>

```
{
  "[Destination](#cfn-datasync-task-taskreportconfig-destination)" : Destination,
  "[ObjectVersionIds](#cfn-datasync-task-taskreportconfig-objectversionids)" : String,
  "[OutputType](#cfn-datasync-task-taskreportconfig-outputtype)" : String,
  "[Overrides](#cfn-datasync-task-taskreportconfig-overrides)" : Overrides,
  "[ReportLevel](#cfn-datasync-task-taskreportconfig-reportlevel)" : String
}
```

### YAML<a name="aws-properties-datasync-task-taskreportconfig-syntax.yaml"></a>

```
  [Destination](#cfn-datasync-task-taskreportconfig-destination): 
    Destination
  [ObjectVersionIds](#cfn-datasync-task-taskreportconfig-objectversionids): String
  [OutputType](#cfn-datasync-task-taskreportconfig-outputtype): String
  [Overrides](#cfn-datasync-task-taskreportconfig-overrides): 
    Overrides
  [ReportLevel](#cfn-datasync-task-taskreportconfig-reportlevel): String
```

## Properties<a name="aws-properties-datasync-task-taskreportconfig-properties"></a>

`Destination`  <a name="cfn-datasync-task-taskreportconfig-destination"></a>
Specifies the Amazon S3 bucket where DataSync uploads your task report\. For more information, see [Task reports](https://docs.aws.amazon.com/datasync/latest/userguide/creating-task-reports.html#task-report-access)\.  
*Required*: Yes  
*Type*: [Destination](aws-properties-datasync-task-destination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObjectVersionIds`  <a name="cfn-datasync-task-taskreportconfig-objectversionids"></a>
Specifies whether your task report includes the new version of each object transferred into an S3 bucket\. This only applies if you [enable versioning on your bucket](https://docs.aws.amazon.com/AmazonS3/latest/userguide/manage-versioning-examples.html)\. Keep in mind that setting this to `INCLUDE` can increase the duration of your task execution\.  
*Required*: No  
*Type*: String  
*Allowed values*: `INCLUDE | NONE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OutputType`  <a name="cfn-datasync-task-taskreportconfig-outputtype"></a>
Specifies the type of task report that you want:  
+  `SUMMARY_ONLY`: Provides necessary details about your task, including the number of files, objects, and directories transferred and transfer duration\.
+  `STANDARD`: Provides complete details about your task, including a full list of files, objects, and directories that were transferred, skipped, verified, and more\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `STANDARD | SUMMARY_ONLY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Overrides`  <a name="cfn-datasync-task-taskreportconfig-overrides"></a>
Customizes the reporting level for aspects of your task report\. For example, your report might generally only include errors, but you could specify that you want a list of successes and errors just for the files that DataSync attempted to delete in your destination location\.  
*Required*: No  
*Type*: [Overrides](aws-properties-datasync-task-overrides.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReportLevel`  <a name="cfn-datasync-task-taskreportconfig-reportlevel"></a>
Specifies whether you want your task report to include only what went wrong with your transfer or a list of what succeeded and didn't\.  
+  `ERRORS_ONLY`: A report shows what DataSync was unable to transfer, skip, verify, and delete\.
+  `SUCCESSES_AND_ERRORS`: A report shows what DataSync was able and unable to transfer, skip, verify, and delete\.
*Required*: No  
*Type*: String  
*Allowed values*: `ERRORS_ONLY | SUCCESSES_AND_ERRORS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)