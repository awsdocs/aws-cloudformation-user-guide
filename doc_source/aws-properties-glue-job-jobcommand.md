# AWS::Glue::Job JobCommand<a name="aws-properties-glue-job-jobcommand"></a>

Specifies code executed when a job is run\.

## Syntax<a name="aws-properties-glue-job-jobcommand-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-job-jobcommand-syntax.json"></a>

```
{
  "[Name](#cfn-glue-job-jobcommand-name)" : String,
  "[PythonVersion](#cfn-glue-job-jobcommand-pythonversion)" : String,
  "[ScriptLocation](#cfn-glue-job-jobcommand-scriptlocation)" : String
}
```

### YAML<a name="aws-properties-glue-job-jobcommand-syntax.yaml"></a>

```
  [Name](#cfn-glue-job-jobcommand-name): String
  [PythonVersion](#cfn-glue-job-jobcommand-pythonversion): String
  [ScriptLocation](#cfn-glue-job-jobcommand-scriptlocation): String
```

## Properties<a name="aws-properties-glue-job-jobcommand-properties"></a>

`Name`  <a name="cfn-glue-job-jobcommand-name"></a>
The name of the job command\. For an Apache Spark ETL job, this must be `glueetl`\. For a Python shell job, it must be `pythonshell`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PythonVersion`  <a name="cfn-glue-job-jobcommand-pythonversion"></a>
The Python version being used to execute a Python shell job\. Allowed values are 2 or 3\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScriptLocation`  <a name="cfn-glue-job-jobcommand-scriptlocation"></a>
Specifies the Amazon Simple Storage Service \(Amazon S3\) path to a script that executes a job \(required\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)