# AWS::Lambda::Function VpcConfig<a name="aws-properties-lambda-function-vpcconfig"></a>

The VPC security groups and subnets that are attached to a Lambda function\. When you connect a function to a VPC, Lambda creates an elastic network interface for each combination of security group and subnet in the function's VPC configuration\. The function can only access resources and the internet through that VPC\. For more information, see [VPC Settings](https://docs.aws.amazon.com/lambda/latest/dg/configuration-vpc.html)\.

**Note**  
When you delete a function, AWS CloudFormation monitors the state of its network interfaces and waits for Lambda to delete them before proceeding\. If the VPC is defined in the same stack, the network interfaces need to be deleted by Lambda before AWS CloudFormation can delete the VPC's resources\.  
To monitor network interfaces, AWS CloudFormation needs the `ec2:DescribeNetworkInterfaces` permission\. It obtains this from the user or role that modifies the stack\. If you don't provide this permission, AWS CloudFormation does not wait for network interfaces to be deleted\.

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

## Examples<a name="aws-properties-lambda-function-vpcconfig--examples"></a>

### VPC Configuration<a name="aws-properties-lambda-function-vpcconfig--examples--VPC_Configuration"></a>

Connect a function to a VPC\.

#### YAML<a name="aws-properties-lambda-function-vpcconfig--examples--VPC_Configuration--yaml"></a>

```
      VpcConfig:
        SecurityGroupIds:
          - sg-085912345678492fb
        SubnetIds:
          - subnet-071f712345678e7c8
          - subnet-07fd123456788a036
```