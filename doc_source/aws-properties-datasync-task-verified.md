# AWS::DataSync::Task Verified<a name="aws-properties-datasync-task-verified"></a>

The reporting level for the verified section of your DataSync task report\.

## Syntax<a name="aws-properties-datasync-task-verified-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datasync-task-verified-syntax.json"></a>

```
{
  "[ReportLevel](#cfn-datasync-task-verified-reportlevel)" : String
}
```

### YAML<a name="aws-properties-datasync-task-verified-syntax.yaml"></a>

```
  [ReportLevel](#cfn-datasync-task-verified-reportlevel): String
```

## Properties<a name="aws-properties-datasync-task-verified-properties"></a>

`ReportLevel`  <a name="cfn-datasync-task-verified-reportlevel"></a>
Specifies whether you want your task report to include only what went wrong with your transfer or a list of what succeeded and didn't\.  
+  `ERRORS_ONLY`: A report shows what DataSync was unable to verify\.
+  `SUCCESSES_AND_ERRORS`: A report shows what DataSync was able and unable to verify\.
*Required*: No  
*Type*: String  
*Allowed values*: `ERRORS_ONLY | SUCCESSES_AND_ERRORS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)