# AWS::SageMaker::ModelBiasJobDefinition NetworkConfig<a name="aws-properties-sagemaker-modelbiasjobdefinition-networkconfig"></a>

Networking options for a job, such as network traffic encryption between containers, whether to allow inbound and outbound network calls to and from containers, and the VPC subnets and security groups to use for VPC\-enabled jobs\.

## Syntax<a name="aws-properties-sagemaker-modelbiasjobdefinition-networkconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelbiasjobdefinition-networkconfig-syntax.json"></a>

```
{
  "[EnableInterContainerTrafficEncryption](#cfn-sagemaker-modelbiasjobdefinition-networkconfig-enableintercontainertrafficencryption)" : Boolean,
  "[EnableNetworkIsolation](#cfn-sagemaker-modelbiasjobdefinition-networkconfig-enablenetworkisolation)" : Boolean,
  "[VpcConfig](#cfn-sagemaker-modelbiasjobdefinition-networkconfig-vpcconfig)" : VpcConfig
}
```

### YAML<a name="aws-properties-sagemaker-modelbiasjobdefinition-networkconfig-syntax.yaml"></a>

```
  [EnableInterContainerTrafficEncryption](#cfn-sagemaker-modelbiasjobdefinition-networkconfig-enableintercontainertrafficencryption): Boolean
  [EnableNetworkIsolation](#cfn-sagemaker-modelbiasjobdefinition-networkconfig-enablenetworkisolation): Boolean
  [VpcConfig](#cfn-sagemaker-modelbiasjobdefinition-networkconfig-vpcconfig): 
    VpcConfig
```

## Properties<a name="aws-properties-sagemaker-modelbiasjobdefinition-networkconfig-properties"></a>

`EnableInterContainerTrafficEncryption`  <a name="cfn-sagemaker-modelbiasjobdefinition-networkconfig-enableintercontainertrafficencryption"></a>
Whether to encrypt all communications between distributed processing jobs\. Choose `True` to encrypt communications\. Encryption provides greater security for distributed processing jobs, but the processing might take longer\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EnableNetworkIsolation`  <a name="cfn-sagemaker-modelbiasjobdefinition-networkconfig-enablenetworkisolation"></a>
Whether to allow inbound and outbound network calls to and from the containers used for the processing job\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcConfig`  <a name="cfn-sagemaker-modelbiasjobdefinition-networkconfig-vpcconfig"></a>
Specifies a VPC that your training jobs and hosted models have access to\. Control access to and from your training and model containers by configuring the VPC\.  
*Required*: No  
*Type*: [VpcConfig](aws-properties-sagemaker-modelbiasjobdefinition-vpcconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)