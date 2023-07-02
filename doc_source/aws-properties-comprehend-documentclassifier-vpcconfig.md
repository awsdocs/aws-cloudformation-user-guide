# AWS::Comprehend::DocumentClassifier VpcConfig<a name="aws-properties-comprehend-documentclassifier-vpcconfig"></a>

 Configuration parameters for an optional private Virtual Private Cloud \(VPC\) containing the resources you are using for the job\. For more information, see [Amazon VPC](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html)\. 

## Syntax<a name="aws-properties-comprehend-documentclassifier-vpcconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-comprehend-documentclassifier-vpcconfig-syntax.json"></a>

```
{
  "[SecurityGroupIds](#cfn-comprehend-documentclassifier-vpcconfig-securitygroupids)" : [ String, ... ],
  "[Subnets](#cfn-comprehend-documentclassifier-vpcconfig-subnets)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-comprehend-documentclassifier-vpcconfig-syntax.yaml"></a>

```
  [SecurityGroupIds](#cfn-comprehend-documentclassifier-vpcconfig-securitygroupids): 
    - String
  [Subnets](#cfn-comprehend-documentclassifier-vpcconfig-subnets): 
    - String
```

## Properties<a name="aws-properties-comprehend-documentclassifier-vpcconfig-properties"></a>

`SecurityGroupIds`  <a name="cfn-comprehend-documentclassifier-vpcconfig-securitygroupids"></a>
The ID number for a security group on an instance of your private VPC\. Security groups on your VPC function serve as a virtual firewall to control inbound and outbound traffic and provides security for the resources that you’ll be accessing on the VPC\. This ID number is preceded by "sg\-", for instance: "sg\-03b388029b0a285ea"\. For more information, see [Security Groups for your VPC](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html)\.   
*Required*: Yes  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Subnets`  <a name="cfn-comprehend-documentclassifier-vpcconfig-subnets"></a>
The ID for each subnet being used in your private VPC\. This subnet is a subset of the a range of IPv4 addresses used by the VPC and is specific to a given availability zone in the VPC’s Region\. This ID number is preceded by "subnet\-", for instance: "subnet\-04ccf456919e69055"\. For more information, see [VPCs and Subnets](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Subnets.html)\.   
*Required*: Yes  
*Type*: List of String  
*Maximum*: `16`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)