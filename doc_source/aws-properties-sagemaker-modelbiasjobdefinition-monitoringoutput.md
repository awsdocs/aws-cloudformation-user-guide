# AWS::SageMaker::ModelBiasJobDefinition MonitoringOutput<a name="aws-properties-sagemaker-modelbiasjobdefinition-monitoringoutput"></a>

The output object for a monitoring job\.

## Syntax<a name="aws-properties-sagemaker-modelbiasjobdefinition-monitoringoutput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelbiasjobdefinition-monitoringoutput-syntax.json"></a>

```
{
  "[S3Output](#cfn-sagemaker-modelbiasjobdefinition-monitoringoutput-s3output)" : S3Output
}
```

### YAML<a name="aws-properties-sagemaker-modelbiasjobdefinition-monitoringoutput-syntax.yaml"></a>

```
  [S3Output](#cfn-sagemaker-modelbiasjobdefinition-monitoringoutput-s3output): 
    S3Output
```

## Properties<a name="aws-properties-sagemaker-modelbiasjobdefinition-monitoringoutput-properties"></a>

`S3Output`  <a name="cfn-sagemaker-modelbiasjobdefinition-monitoringoutput-s3output"></a>
The Amazon S3 storage location where the results of a monitoring job are saved\.  
*Required*: Yes  
*Type*: [S3Output](aws-properties-sagemaker-modelbiasjobdefinition-s3output.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)