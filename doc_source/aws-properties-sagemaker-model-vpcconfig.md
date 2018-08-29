# Amazon SageMaker Model VpcConfig<a name="aws-properties-sagemaker-model-vpcconfig"></a>

<a name="aws-properties-sagemaker-model-vpcconfig-description"></a>The `VpcConfig` property type specifies a VPC that your hosted models have access to\. Control access to and from your training and model containers by configuring the VPC\. For more information, see [Protect Models by Using an Amazon Virtual Private Cloud](http://docs.aws.amazon.com//sagemaker/latest/dg/host-vpc.html)\.

<a name="aws-properties-sagemaker-model-vpcconfig-inheritance"></a> `VpcConfig` is a property of the [AWS::SageMaker::Model](aws-resource-sagemaker-model.md) resource\.

## Syntax<a name="aws-properties-sagemaker-model-vpcconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-model-vpcconfig-syntax.json"></a>

```
{
  "[Subnets](#cfn-sagemaker-model-vpcconfig-subnets)" : [String, ... ],
  "[SecurityGroupIds](#cfn-sagemaker-model-vpcconfig-securitygroupids): [String, ... ]
}
```

### YAML<a name="aws-properties-sagemaker-model-vpcconfig-syntax.yaml"></a>

```
[Subnets](#cfn-sagemaker-model-vpcconfig-subnets): 
    - String
[SecurityGroupIds](#cfn-sagemaker-model-vpcconfig-securitygroupids): 
    - String
```

## Properties<a name="aws-properties-sagemaker-model-vpcconfig-properties"></a>

`Subnets`  <a name="cfn-sagemaker-model-vpcconfig-subnets"></a>
The ID of the subnets in the VPC to which you want to connect your training job or model\.   
 *Required*: Yes  
 *Type*: List of String values  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`SecurityGroupIds`  <a name="cfn-sagemaker-model-vpcconfig-securitygroupids"></a>
The VPC security group IDs, in the form sg\-xxxxxxxx\. Specify the security groups for the VPC that is specified in the Subnets field\.   
 *Required*: Yes  
 *Type*: List of String values  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 