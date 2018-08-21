# AWS Lambda Function VpcConfig<a name="aws-properties-lambda-function-vpcconfig"></a>

`VpcConfig` is a property of the [AWS::Lambda::Function](aws-resource-lambda-function.md) resource that enables your AWS Lambda \(Lambda\) function to access resources in a VPC\. For more information, see [Configuring a Lambda Function to Access Resources in an Amazon VPC](http://docs.aws.amazon.com/lambda/latest/dg/vpc.html) in the *AWS Lambda Developer Guide*\.

## Syntax<a name="w3ab2c21c14e1537b5"></a>

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

## Properties<a name="w3ab2c21c14e1537b7"></a>

`SecurityGroupIds`  <a name="cfn-lambda-function-vpcconfig-securitygroupids"></a>
A list of one or more security groups IDs in the VPC that includes the resources to which your Lambda function requires access\.  
*Required*: Yes  
*Type*: List of String values

`SubnetIds`  <a name="cfn-lambda-function-vpcconfig-subnetids"></a>
A list of one or more subnet IDs in the VPC that includes the resources to which your Lambda function requires access\.  
*Required*: Yes  
*Type*: List of String values