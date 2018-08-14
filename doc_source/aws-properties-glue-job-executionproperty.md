# AWS Glue Job ExecutionProperty<a name="aws-properties-glue-job-executionproperty"></a>

<a name="aws-properties-glue-job-executionproperty-description"></a>The `ExecutionProperty` property type specifies the maximum number of concurrent runs allowed for an AWS Glue job\.

<a name="aws-properties-glue-job-executionproperty-inheritance"></a> `ExecutionProperty` is a property of the [AWS::Glue::Job](aws-resource-glue-job.md) resource\.

## Syntax<a name="aws-properties-glue-job-executionproperty-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-job-executionproperty-syntax.json"></a>

```
{
  "[MaxConcurrentRuns](#cfn-glue-job-executionproperty-maxconcurrentruns)" : Integer
}
```

### YAML<a name="aws-properties-glue-job-executionproperty-syntax.yaml"></a>

```
[MaxConcurrentRuns](#cfn-glue-job-executionproperty-maxconcurrentruns): Integer
```

## Properties<a name="aws-properties-glue-job-executionproperty-properties"></a>

For more information, see [ExecutionProperty Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-job.html#aws-glue-api-jobs-job-ExecutionProperty) in the *AWS Glue Developer Guide*\.

`MaxConcurrentRuns`  <a name="cfn-glue-job-executionproperty-maxconcurrentruns"></a>
The maximum number of concurrent runs that are allowed for the job\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 