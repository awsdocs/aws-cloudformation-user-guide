# AWS::DataSync::Task Deleted<a name="aws-properties-datasync-task-deleted"></a>

The reporting level for the deleted section of your DataSync task report\.

## Syntax<a name="aws-properties-datasync-task-deleted-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datasync-task-deleted-syntax.json"></a>

```
{
  "[ReportLevel](#cfn-datasync-task-deleted-reportlevel)" : String
}
```

### YAML<a name="aws-properties-datasync-task-deleted-syntax.yaml"></a>

```
  [ReportLevel](#cfn-datasync-task-deleted-reportlevel): String
```

## Properties<a name="aws-properties-datasync-task-deleted-properties"></a>

`ReportLevel`  <a name="cfn-datasync-task-deleted-reportlevel"></a>
Specifies whether you want your task report to include only what went wrong with your transfer or a list of what succeeded and didn't\.  
+  `ERRORS_ONLY`: A report shows what DataSync was unable to delete\.
+  `SUCCESSES_AND_ERRORS`: A report shows what DataSync was able and unable to delete\.
*Required*: No  
*Type*: String  
*Allowed values*: `ERRORS_ONLY | SUCCESSES_AND_ERRORS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)