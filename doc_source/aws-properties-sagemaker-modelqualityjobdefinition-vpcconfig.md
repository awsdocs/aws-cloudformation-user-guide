# AWS::SageMaker::ModelQualityJobDefinition VpcConfig<a name="aws-properties-sagemaker-modelqualityjobdefinition-vpcconfig"></a>

Specifies a VPC that your training jobs and hosted models have access to\. Control access to and from your training and model containers by configuring the VPC\. For more information, see [Protect Endpoints by Using an Amazon Virtual Private Cloud](https://docs.aws.amazon.com/sagemaker/latest/dg/host-vpc.html) and [Protect Training Jobs by Using an Amazon Virtual Private Cloud](https://docs.aws.amazon.com/sagemaker/latest/dg/train-vpc.html)\. 

## Syntax<a name="aws-properties-sagemaker-modelqualityjobdefinition-vpcconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-modelqualityjobdefinition-vpcconfig-syntax.json"></a>

```
{
  "[SecurityGroupIds](#cfn-sagemaker-modelqualityjobdefinition-vpcconfig-securitygroupids)" : [ String, ... ],
  "[Subnets](#cfn-sagemaker-modelqualityjobdefinition-vpcconfig-subnets)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-sagemaker-modelqualityjobdefinition-vpcconfig-syntax.yaml"></a>

```
  [SecurityGroupIds](#cfn-sagemaker-modelqualityjobdefinition-vpcconfig-securitygroupids): 
    - String
  [Subnets](#cfn-sagemaker-modelqualityjobdefinition-vpcconfig-subnets): 
    - String
```

## Properties<a name="aws-properties-sagemaker-modelqualityjobdefinition-vpcconfig-properties"></a>

`SecurityGroupIds`  <a name="cfn-sagemaker-modelqualityjobdefinition-vpcconfig-securitygroupids"></a>
The VPC security group IDs, in the form sg\-xxxxxxxx\. Specify the security groups for the VPC that is specified in the `Subnets` field\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Subnets`  <a name="cfn-sagemaker-modelqualityjobdefinition-vpcconfig-subnets"></a>
The ID of the subnets in the VPC to which you want to connect your training job or model\. For information about the availability of specific instance types, see [Supported Instance Types and Availability Zones](https://docs.aws.amazon.com/sagemaker/latest/dg/instance-types-az.html)\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `16`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)