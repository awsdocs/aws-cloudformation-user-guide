# AWS::Lambda::Function VpcConfig<a name="aws-properties-lambda-function-vpcconfig"></a>

The VPC security groups and subnets that are attached to a Lambda function\.

## Syntax<a name="aws-properties-lambda-function-vpcconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-function-vpcconfig-syntax.json"></a>

```
{
  "[SecurityGroupIds](#cfn-lambda-function-vpcconfig-securitygroupids)" : [ String, ... ],
  "[SubnetIds](#cfn-lambda-function-vpcconfig-subnetids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-lambda-function-vpcconfig-syntax.yaml"></a>

```
  [SecurityGroupIds](#cfn-lambda-function-vpcconfig-securitygroupids): 
    - String
  [SubnetIds](#cfn-lambda-function-vpcconfig-subnetids): 
    - String
```

## Properties<a name="aws-properties-lambda-function-vpcconfig-properties"></a>

`SecurityGroupIds`  <a name="cfn-lambda-function-vpcconfig-securitygroupids"></a>
A list of VPC security groups IDs\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-lambda-function-vpcconfig-subnetids"></a>
A list of VPC subnet IDs\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `16`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by ***all*** regions.