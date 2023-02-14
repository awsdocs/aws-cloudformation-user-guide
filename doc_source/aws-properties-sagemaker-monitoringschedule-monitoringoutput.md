# AWS::SageMaker::MonitoringSchedule MonitoringOutput<a name="aws-properties-sagemaker-monitoringschedule-monitoringoutput"></a>

The output object for a monitoring job\.

## Syntax<a name="aws-properties-sagemaker-monitoringschedule-monitoringoutput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-monitoringschedule-monitoringoutput-syntax.json"></a>

```
{
  "[S3Output](#cfn-sagemaker-monitoringschedule-monitoringoutput-s3output)" : S3Output
}
```

### YAML<a name="aws-properties-sagemaker-monitoringschedule-monitoringoutput-syntax.yaml"></a>

```
  [S3Output](#cfn-sagemaker-monitoringschedule-monitoringoutput-s3output): 
    S3Output
```

## Properties<a name="aws-properties-sagemaker-monitoringschedule-monitoringoutput-properties"></a>

`S3Output`  <a name="cfn-sagemaker-monitoringschedule-monitoringoutput-s3output"></a>
The Amazon S3 storage location where the results of a monitoring job are saved\.  
*Required*: Yes  
*Type*: [S3Output](aws-properties-sagemaker-monitoringschedule-s3output.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)