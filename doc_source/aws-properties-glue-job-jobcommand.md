# AWS Glue Job JobCommand<a name="aws-properties-glue-job-jobcommand"></a>

<a name="aws-properties-glue-job-jobcommand-description"></a>The `JobCommand` property type specifies code that executes an AWS Glue job\.

<a name="aws-properties-glue-job-jobcommand-inheritance"></a> `JobCommand` is the property type for the `Command` property of the [AWS::Glue::Job](aws-resource-glue-job.md) resource\.

## Syntax<a name="aws-properties-glue-job-jobcommand-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-job-jobcommand-syntax.json"></a>

```
{
  "[ScriptLocation](#cfn-glue-job-jobcommand-scriptlocation)" : String,
  "[Name](#cfn-glue-job-jobcommand-name)" : String
}
```

### YAML<a name="aws-properties-glue-job-jobcommand-syntax.yaml"></a>

```
[ScriptLocation](#cfn-glue-job-jobcommand-scriptlocation): String
[Name](#cfn-glue-job-jobcommand-name): String
```

## Properties<a name="aws-properties-glue-job-jobcommand-properties"></a>

For more information, see [JobCommand Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-job.html#aws-glue-api-jobs-job-JobCommand) in the *AWS Glue Developer Guide*\.

`ScriptLocation`  <a name="cfn-glue-job-jobcommand-scriptlocation"></a>
The location of a script that executes a job\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-glue-job-jobcommand-name"></a>
The name of the job command\.  
 *Required*: No  
 *Type*: String  
 *Valid values*: `glueetl`  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 