# AWS::GreengrassV2::ComponentVersion LambdaLinuxProcessParams<a name="aws-properties-greengrassv2-componentversion-lambdalinuxprocessparams"></a>

Contains parameters for a Linux process that contains an AWS Lambda function\.

## Syntax<a name="aws-properties-greengrassv2-componentversion-lambdalinuxprocessparams-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrassv2-componentversion-lambdalinuxprocessparams-syntax.json"></a>

```
{
  "[ContainerParams](#cfn-greengrassv2-componentversion-lambdalinuxprocessparams-containerparams)" : LambdaContainerParams,
  "[IsolationMode](#cfn-greengrassv2-componentversion-lambdalinuxprocessparams-isolationmode)" : String
}
```

### YAML<a name="aws-properties-greengrassv2-componentversion-lambdalinuxprocessparams-syntax.yaml"></a>

```
  [ContainerParams](#cfn-greengrassv2-componentversion-lambdalinuxprocessparams-containerparams): 
    LambdaContainerParams
  [IsolationMode](#cfn-greengrassv2-componentversion-lambdalinuxprocessparams-isolationmode): String
```

## Properties<a name="aws-properties-greengrassv2-componentversion-lambdalinuxprocessparams-properties"></a>

`ContainerParams`  <a name="cfn-greengrassv2-componentversion-lambdalinuxprocessparams-containerparams"></a>
The parameters for the container in which the Lambda function runs\.  
*Required*: No  
*Type*: [LambdaContainerParams](aws-properties-greengrassv2-componentversion-lambdacontainerparams.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IsolationMode`  <a name="cfn-greengrassv2-componentversion-lambdalinuxprocessparams-isolationmode"></a>
The isolation mode for the process that contains the Lambda function\. The process can run in an isolated runtime environment inside the AWS IoT Greengrass container, or as a regular process outside any container\.  
Default: `GreengrassContainer`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)