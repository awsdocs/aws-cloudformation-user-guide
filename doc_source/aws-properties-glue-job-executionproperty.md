# AWS::Glue::Job ExecutionProperty<a name="aws-properties-glue-job-executionproperty"></a>

An execution property of a job\.

## Syntax<a name="aws-properties-glue-job-executionproperty-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-job-executionproperty-syntax.json"></a>

```
{
  "[MaxConcurrentRuns](#cfn-glue-job-executionproperty-maxconcurrentruns)" : Double
}
```

### YAML<a name="aws-properties-glue-job-executionproperty-syntax.yaml"></a>

```
  [MaxConcurrentRuns](#cfn-glue-job-executionproperty-maxconcurrentruns): Double
```

## Properties<a name="aws-properties-glue-job-executionproperty-properties"></a>

`MaxConcurrentRuns`  <a name="cfn-glue-job-executionproperty-maxconcurrentruns"></a>
The maximum number of concurrent runs allowed for the job\. The default is 1\. An error is returned when this threshold is reached\. The maximum value you can specify is controlled by a service limit\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)