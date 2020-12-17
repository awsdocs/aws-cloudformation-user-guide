# AWS::AppSync::Resolver PipelineConfig<a name="aws-properties-appsync-resolver-pipelineconfig"></a>

Use the `PipelineConfig` property type to specify `PipelineConfig` for an AWS AppSync resolver\.

 `PipelineConfig` is a property of the [AWS::AppSync::Resolver](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-resolver.html) resource\.

## Syntax<a name="aws-properties-appsync-resolver-pipelineconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-resolver-pipelineconfig-syntax.json"></a>

```
{
  "[Functions](#cfn-appsync-resolver-pipelineconfig-functions)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-appsync-resolver-pipelineconfig-syntax.yaml"></a>

```
  [Functions](#cfn-appsync-resolver-pipelineconfig-functions): 
    - String
```

## Properties<a name="aws-properties-appsync-resolver-pipelineconfig-properties"></a>

`Functions`  <a name="cfn-appsync-resolver-pipelineconfig-functions"></a>
A list of `Function` objects\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)