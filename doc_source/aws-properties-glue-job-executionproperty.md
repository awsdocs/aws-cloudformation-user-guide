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

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-north-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
