# AWS::SageMaker::EndpointConfig ProductionVariant<a name="aws-properties-sagemaker-endpointconfig-productionvariant"></a>

Specifies a model that you want to host and the resources to deploy for hosting it\. If you are deploying multiple models, tell Amazon SageMaker how to distribute traffic among the models by specifying the `InitialVariantWeight` objects\. 

## Syntax<a name="aws-properties-sagemaker-endpointconfig-productionvariant-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-endpointconfig-productionvariant-syntax.json"></a>

```
{
  "[AcceleratorType](#cfn-sagemaker-endpointconfig-productionvariant-acceleratortype)" : String,
  "[ContainerStartupHealthCheckTimeoutInSeconds](#cfn-sagemaker-endpointconfig-productionvariant-containerstartuphealthchecktimeoutinseconds)" : Integer,
  "[InitialInstanceCount](#cfn-sagemaker-endpointconfig-productionvariant-initialinstancecount)" : Integer,
  "[InitialVariantWeight](#cfn-sagemaker-endpointconfig-productionvariant-initialvariantweight)" : Double,
  "[InstanceType](#cfn-sagemaker-endpointconfig-productionvariant-instancetype)" : String,
  "[ModelDataDownloadTimeoutInSeconds](#cfn-sagemaker-endpointconfig-productionvariant-modeldatadownloadtimeoutinseconds)" : Integer,
  "[ModelName](#cfn-sagemaker-endpointconfig-productionvariant-modelname)" : String,
  "[ServerlessConfig](#cfn-sagemaker-endpointconfig-productionvariant-serverlessconfig)" : ServerlessConfig,
  "[VariantName](#cfn-sagemaker-endpointconfig-productionvariant-variantname)" : String,
  "[VolumeSizeInGB](#cfn-sagemaker-endpointconfig-productionvariant-volumesizeingb)" : Integer
}
```

### YAML<a name="aws-properties-sagemaker-endpointconfig-productionvariant-syntax.yaml"></a>

```
  [AcceleratorType](#cfn-sagemaker-endpointconfig-productionvariant-acceleratortype): String
  [ContainerStartupHealthCheckTimeoutInSeconds](#cfn-sagemaker-endpointconfig-productionvariant-containerstartuphealthchecktimeoutinseconds): Integer
  [InitialInstanceCount](#cfn-sagemaker-endpointconfig-productionvariant-initialinstancecount): Integer
  [InitialVariantWeight](#cfn-sagemaker-endpointconfig-productionvariant-initialvariantweight): Double
  [InstanceType](#cfn-sagemaker-endpointconfig-productionvariant-instancetype): String
  [ModelDataDownloadTimeoutInSeconds](#cfn-sagemaker-endpointconfig-productionvariant-modeldatadownloadtimeoutinseconds): Integer
  [ModelName](#cfn-sagemaker-endpointconfig-productionvariant-modelname): String
  [ServerlessConfig](#cfn-sagemaker-endpointconfig-productionvariant-serverlessconfig): 
    ServerlessConfig
  [VariantName](#cfn-sagemaker-endpointconfig-productionvariant-variantname): String
  [VolumeSizeInGB](#cfn-sagemaker-endpointconfig-productionvariant-volumesizeingb): Integer
```

## Properties<a name="aws-properties-sagemaker-endpointconfig-productionvariant-properties"></a>

`AcceleratorType`  <a name="cfn-sagemaker-endpointconfig-productionvariant-acceleratortype"></a>
The size of the Elastic Inference \(EI\) instance to use for the production variant\. EI instances provide on\-demand GPU computing for inference\. For more information, see [Using Elastic Inference in Amazon SageMaker](https://docs.aws.amazon.com/sagemaker/latest/dg/ei.html)\. For more information, see [Using Elastic Inference in Amazon SageMaker](https://docs.aws.amazon.com/sagemaker/latest/dg/ei.html)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ml.eia1.large | ml.eia1.medium | ml.eia1.xlarge | ml.eia2.large | ml.eia2.medium | ml.eia2.xlarge`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ContainerStartupHealthCheckTimeoutInSeconds`  <a name="cfn-sagemaker-endpointconfig-productionvariant-containerstartuphealthchecktimeoutinseconds"></a>
Property description not available\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InitialInstanceCount`  <a name="cfn-sagemaker-endpointconfig-productionvariant-initialinstancecount"></a>
Number of instances to launch initially\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InitialVariantWeight`  <a name="cfn-sagemaker-endpointconfig-productionvariant-initialvariantweight"></a>
Determines initial traffic distribution among all of the models that you specify in the endpoint configuration\. The traffic to a production variant is determined by the ratio of the `VariantWeight` to the sum of all `VariantWeight` values across all ProductionVariants\. If unspecified, it defaults to 1\.0\.   
*Required*: Yes  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceType`  <a name="cfn-sagemaker-endpointconfig-productionvariant-instancetype"></a>
The ML compute instance type\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ml.c4.2xlarge | ml.c4.4xlarge | ml.c4.8xlarge | ml.c4.large | ml.c4.xlarge | ml.c5.18xlarge | ml.c5.2xlarge | ml.c5.4xlarge | ml.c5.9xlarge | ml.c5.large | ml.c5.xlarge | ml.c5d.18xlarge | ml.c5d.2xlarge | ml.c5d.4xlarge | ml.c5d.9xlarge | ml.c5d.large | ml.c5d.xlarge | ml.c6g.12xlarge | ml.c6g.16xlarge | ml.c6g.2xlarge | ml.c6g.4xlarge | ml.c6g.8xlarge | ml.c6g.large | ml.c6g.xlarge | ml.c6gd.12xlarge | ml.c6gd.16xlarge | ml.c6gd.2xlarge | ml.c6gd.4xlarge | ml.c6gd.8xlarge | ml.c6gd.large | ml.c6gd.xlarge | ml.c6gn.12xlarge | ml.c6gn.16xlarge | ml.c6gn.2xlarge | ml.c6gn.4xlarge | ml.c6gn.8xlarge | ml.c6gn.large | ml.c6gn.xlarge | ml.c6i.12xlarge | ml.c6i.16xlarge | ml.c6i.24xlarge | ml.c6i.2xlarge | ml.c6i.32xlarge | ml.c6i.4xlarge | ml.c6i.8xlarge | ml.c6i.large | ml.c6i.xlarge | ml.c7g.12xlarge | ml.c7g.16xlarge | ml.c7g.2xlarge | ml.c7g.4xlarge | ml.c7g.8xlarge | ml.c7g.large | ml.c7g.xlarge | ml.g4dn.12xlarge | ml.g4dn.16xlarge | ml.g4dn.2xlarge | ml.g4dn.4xlarge | ml.g4dn.8xlarge | ml.g4dn.xlarge | ml.g5.12xlarge | ml.g5.16xlarge | ml.g5.24xlarge | ml.g5.2xlarge | ml.g5.48xlarge | ml.g5.4xlarge | ml.g5.8xlarge | ml.g5.xlarge | ml.inf1.24xlarge | ml.inf1.2xlarge | ml.inf1.6xlarge | ml.inf1.xlarge | ml.m4.10xlarge | ml.m4.16xlarge | ml.m4.2xlarge | ml.m4.4xlarge | ml.m4.xlarge | ml.m5.12xlarge | ml.m5.24xlarge | ml.m5.2xlarge | ml.m5.4xlarge | ml.m5.large | ml.m5.xlarge | ml.m5d.12xlarge | ml.m5d.24xlarge | ml.m5d.2xlarge | ml.m5d.4xlarge | ml.m5d.large | ml.m5d.xlarge | ml.m6g.12xlarge | ml.m6g.16xlarge | ml.m6g.2xlarge | ml.m6g.4xlarge | ml.m6g.8xlarge | ml.m6g.large | ml.m6g.xlarge | ml.m6gd.12xlarge | ml.m6gd.16xlarge | ml.m6gd.2xlarge | ml.m6gd.4xlarge | ml.m6gd.8xlarge | ml.m6gd.large | ml.m6gd.xlarge | ml.p2.16xlarge | ml.p2.8xlarge | ml.p2.xlarge | ml.p3.16xlarge | ml.p3.2xlarge | ml.p3.8xlarge | ml.p4d.24xlarge | ml.p4de.24xlarge | ml.r5.12xlarge | ml.r5.24xlarge | ml.r5.2xlarge | ml.r5.4xlarge | ml.r5.large | ml.r5.xlarge | ml.r5d.12xlarge | ml.r5d.24xlarge | ml.r5d.2xlarge | ml.r5d.4xlarge | ml.r5d.large | ml.r5d.xlarge | ml.r6g.12xlarge | ml.r6g.16xlarge | ml.r6g.2xlarge | ml.r6g.4xlarge | ml.r6g.8xlarge | ml.r6g.large | ml.r6g.xlarge | ml.r6gd.12xlarge | ml.r6gd.16xlarge | ml.r6gd.2xlarge | ml.r6gd.4xlarge | ml.r6gd.8xlarge | ml.r6gd.large | ml.r6gd.xlarge | ml.t2.2xlarge | ml.t2.large | ml.t2.medium | ml.t2.xlarge`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelDataDownloadTimeoutInSeconds`  <a name="cfn-sagemaker-endpointconfig-productionvariant-modeldatadownloadtimeoutinseconds"></a>
Property description not available\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ModelName`  <a name="cfn-sagemaker-endpointconfig-productionvariant-modelname"></a>
The name of the model that you want to host\. This is the name that you specified when creating the model\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9])*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServerlessConfig`  <a name="cfn-sagemaker-endpointconfig-productionvariant-serverlessconfig"></a>
The serverless configuration for an endpoint\. Specifies a serverless endpoint configuration instead of an instance\-based endpoint configuration\.  
*Required*: No  
*Type*: [ServerlessConfig](aws-properties-sagemaker-endpointconfig-productionvariant-serverlessconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VariantName`  <a name="cfn-sagemaker-endpointconfig-productionvariant-variantname"></a>
The name of the production variant\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9](-*[a-zA-Z0-9]){0,62}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VolumeSizeInGB`  <a name="cfn-sagemaker-endpointconfig-productionvariant-volumesizeingb"></a>
Property description not available\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)