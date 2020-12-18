# AWS::CodeBuild::Project VpcConfig<a name="aws-properties-codebuild-project-vpcconfig"></a>

 `VpcConfig` is a property of the [AWS::CodeBuild::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html) resource that enable AWS CodeBuild to access resources in an Amazon VPC\. For more information, see [Use AWS CodeBuild with Amazon Virtual Private Cloud](https://docs.aws.amazon.com/codebuild/latest/userguide/vpc-support.html) in the *AWS CodeBuild User Guide*\. 

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
A list of one or more security groups IDs in your Amazon VPC\. The maximum count is 5\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subnets`  <a name="cfn-codebuild-project-vpcconfig-subnets"></a>
A list of one or more subnet IDs in your Amazon VPC\. The maximum count is 16\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `16`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-codebuild-project-vpcconfig-vpcid"></a>
The ID of the Amazon VPC\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-codebuild-project-vpcconfig--seealso"></a>
+  [ VpcConfig](https://docs.aws.amazon.com/codebuild/latest/APIReference/API_VpcConfig.html) in the *AWS CodeBuild API Reference* 