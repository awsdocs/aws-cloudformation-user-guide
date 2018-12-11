# AWS AppSync Resolver PipelineConfig<a name="aws-properties-appsync-resolver-pipelineconfig"></a>

<a name="aws-properties-appsync-resolver-pipelineconfig-description"></a>Use the `PipelineConfig` property type to specify PipelineConfig for an AWS AppSync resolver\.

<a name="aws-properties-appsync-resolver-pipelineconfig-inheritance"></a> `PipelineConfig` is a property of the [AWS::AppSync::Resolver](aws-resource-appsync-resolver.md) resource\.

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
The FunctionsIds of the functions attached with the resolver\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-appsync-resolver-pipelineconfig-seealso"></a>
+ [ PipelineResolverConfig](https://docs.aws.amazon.com/appsync/latest/APIReference/API_PipelineConfig.html) operation in the *AWS AppSync API Reference*