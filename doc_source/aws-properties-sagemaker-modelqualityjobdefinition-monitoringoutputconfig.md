# AWS::SageMaker::ModelQualityJobDefinition MonitoringOutputConfig<a name="aws-properties-sagemaker-modelqualityjobdefinition-monitoringoutputconfig"></a>

The output configuration for monitoring jobs\.

## Syntax<a name="aws-properties-sagemaker-modelqualityjobdefinition-monitoringoutputconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelqualityjobdefinition-monitoringoutputconfig-syntax.json"></a>

```
{
  "[KmsKeyId](#cfn-sagemaker-modelqualityjobdefinition-monitoringoutputconfig-kmskeyid)" : String,
  "[MonitoringOutputs](#cfn-sagemaker-modelqualityjobdefinition-monitoringoutputconfig-monitoringoutputs)" : [ MonitoringOutput, ... ]
}
```

### YAML<a name="aws-properties-sagemaker-modelqualityjobdefinition-monitoringoutputconfig-syntax.yaml"></a>

```
  [KmsKeyId](#cfn-sagemaker-modelqualityjobdefinition-monitoringoutputconfig-kmskeyid): String
  [MonitoringOutputs](#cfn-sagemaker-modelqualityjobdefinition-monitoringoutputconfig-monitoringoutputs): 
    - MonitoringOutput
```

## Properties<a name="aws-properties-sagemaker-modelqualityjobdefinition-monitoringoutputconfig-properties"></a>

`KmsKeyId`  <a name="cfn-sagemaker-modelqualityjobdefinition-monitoringoutputconfig-kmskeyid"></a>
The AWS Key Management Service \(AWS KMS\) key that Amazon SageMaker uses to encrypt the model artifacts at rest using Amazon S3 server\-side encryption\.  
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Pattern*: `.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MonitoringOutputs`  <a name="cfn-sagemaker-modelqualityjobdefinition-monitoringoutputconfig-monitoringoutputs"></a>
Monitoring outputs for monitoring jobs\. This is where the output of the periodic monitoring jobs is uploaded\.  
*Required*: Yes  
*Type*: List of [MonitoringOutput](aws-properties-sagemaker-modelqualityjobdefinition-monitoringoutput.md)  
*Maximum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)