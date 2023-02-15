# AWS::SageMaker::ModelBiasJobDefinition MonitoringGroundTruthS3Input<a name="aws-properties-sagemaker-modelbiasjobdefinition-monitoringgroundtruths3input"></a>

The ground truth labels for the dataset used for the monitoring job\.

## Syntax<a name="aws-properties-sagemaker-modelbiasjobdefinition-monitoringgroundtruths3input-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelbiasjobdefinition-monitoringgroundtruths3input-syntax.json"></a>

```
{
  "[S3Uri](#cfn-sagemaker-modelbiasjobdefinition-monitoringgroundtruths3input-s3uri)" : String
}
```

### YAML<a name="aws-properties-sagemaker-modelbiasjobdefinition-monitoringgroundtruths3input-syntax.yaml"></a>

```
  [S3Uri](#cfn-sagemaker-modelbiasjobdefinition-monitoringgroundtruths3input-s3uri): String
```

## Properties<a name="aws-properties-sagemaker-modelbiasjobdefinition-monitoringgroundtruths3input-properties"></a>

`S3Uri`  <a name="cfn-sagemaker-modelbiasjobdefinition-monitoringgroundtruths3input-s3uri"></a>
The address of the Amazon S3 location of the ground truth labels\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `^(https|s3)://([^/]+)/?(.*)$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)