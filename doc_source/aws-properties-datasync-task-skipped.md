# AWS::DataSync::Task Skipped<a name="aws-properties-datasync-task-skipped"></a>

The reporting level for the skipped section of your DataSync task report\.

## Syntax<a name="aws-properties-datasync-task-skipped-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datasync-task-skipped-syntax.json"></a>

```
{
  "[ReportLevel](#cfn-datasync-task-skipped-reportlevel)" : String
}
```

### YAML<a name="aws-properties-datasync-task-skipped-syntax.yaml"></a>

```
  [ReportLevel](#cfn-datasync-task-skipped-reportlevel): String
```

## Properties<a name="aws-properties-datasync-task-skipped-properties"></a>

`ReportLevel`  <a name="cfn-datasync-task-skipped-reportlevel"></a>
Specifies whether you want your task report to include only what went wrong with your transfer or a list of what succeeded and didn't\.  
+  `ERRORS_ONLY`: A report shows what DataSync was unable to skip\.
+  `SUCCESSES_AND_ERRORS`: A report shows what DataSync was able and unable to skip\.
*Required*: No  
*Type*: String  
*Allowed values*: `ERRORS_ONLY | SUCCESSES_AND_ERRORS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)