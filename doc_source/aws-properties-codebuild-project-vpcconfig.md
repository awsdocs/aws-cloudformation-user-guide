# AWS CodeBuild Project VpcConfig<a name="aws-properties-codebuild-project-vpcconfig"></a>

<a name="aws-properties-codebuild-project-vpcconfig-description"></a>The `VpcConfig` property type specifies settings that enable AWS CodeBuild to access resources in an Amazon VPC\.

<a name="aws-properties-codebuild-project-vpcconfig-inheritance"></a> `VpcConfig` is a property of the [AWS::CodeBuild::Project](aws-resource-codebuild-project.md) resource\.

## Syntax<a name="aws-properties-codebuild-project-vpcconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-project-vpcconfig-syntax.json"></a>

```
{
  "[SecurityGroupIds](#cfn-codebuild-project-vpcconfig-securitygroupids)" : [ String, ... ],
  "[Subnets](#cfn-codebuild-project-vpcconfig-subnets)" : [ String, ... ],
  "[VpcId](#cfn-codebuild-project-vpcconfig-vpcid)" : String
}
```

### YAML<a name="aws-properties-codebuild-project-vpcconfig-syntax.yaml"></a>

```
[SecurityGroupIds](#cfn-codebuild-project-vpcconfig-securitygroupids): 
  - String
[Subnets](#cfn-codebuild-project-vpcconfig-subnets): 
  - String
[VpcId](#cfn-codebuild-project-vpcconfig-vpcid): String
```

## Properties<a name="aws-properties-codebuild-project-vpcconfig-properties"></a>

`SecurityGroupIds`  <a name="cfn-codebuild-project-vpcconfig-securitygroupids"></a>
The IDs of the security groups in the Amazon VPC\. The maximum count is 5\.  
 *Required*: Yes  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Subnets`  <a name="cfn-codebuild-project-vpcconfig-subnets"></a>
The IDs of the subnets in the Amazon VPC\. The maximum count is 16\.  
 *Required*: Yes  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`VpcId`  <a name="cfn-codebuild-project-vpcconfig-vpcid"></a>
The ID of the Amazon VPC\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-codebuild-project-vpcconfig-seealso"></a>
+ [ VpcConfig](http://docs.aws.amazon.com/codebuild/latest/APIReference/API_VpcConfig.html) in the *AWS CodeBuild API Reference*