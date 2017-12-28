# AWS Glue Job ExecutionProperty<a name="aws-properties-glue-job-executionproperty"></a>

<a name="aws-properties-glue-job-executionproperty-description"></a>The `ExecutionProperty` property type specifies the maximum number of concurrent runs allowed for an AWS Glue job\.

<a name="aws-properties-glue-job-executionproperty-inheritance"></a> `ExecutionProperty` is a property of the [AWS::Glue::Job](aws-resource-glue-job.md) resource\.

## Syntax<a name="aws-properties-glue-job-executionproperty-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-job-executionproperty-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-job-executionproperty-maxconcurrentruns)" : Double
}
```

### YAML<a name="aws-properties-glue-job-executionproperty-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-glue-job-executionproperty-maxconcurrentruns): Double
```

## Properties<a name="aws-properties-glue-job-executionproperty-properties"></a>

For more information, see [ExecutionProperty Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-job.html#aws-glue-api-jobs-job-ExecutionProperty) in the *AWS Glue Developer Guide*\.

`MaxConcurrentRuns`  
The maximum number of concurrent runs that are allowed for the job\.  
 *Required*: No  
 *Type*: Double  
 *Update requires*: No interruption 