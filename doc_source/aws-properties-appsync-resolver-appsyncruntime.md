# AWS::AppSync::Resolver AppSyncRuntime<a name="aws-properties-appsync-resolver-appsyncruntime"></a>

Describes a runtime used by an AWS AppSync pipeline resolver or AWS AppSync function\. Specifies the name and version of the runtime to use\. Note that if a runtime is specified, code must also be specified\.

## Syntax<a name="aws-properties-appsync-resolver-appsyncruntime-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-resolver-appsyncruntime-syntax.json"></a>

```
{
  "[Name](#cfn-appsync-resolver-appsyncruntime-name)" : String,
  "[RuntimeVersion](#cfn-appsync-resolver-appsyncruntime-runtimeversion)" : String
}
```

### YAML<a name="aws-properties-appsync-resolver-appsyncruntime-syntax.yaml"></a>

```
  [Name](#cfn-appsync-resolver-appsyncruntime-name): String
  [RuntimeVersion](#cfn-appsync-resolver-appsyncruntime-runtimeversion): String
```

## Properties<a name="aws-properties-appsync-resolver-appsyncruntime-properties"></a>

`Name`  <a name="cfn-appsync-resolver-appsyncruntime-name"></a>
The `name` of the runtime to use\. Currently, the only allowed value is `APPSYNC_JS`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuntimeVersion`  <a name="cfn-appsync-resolver-appsyncruntime-runtimeversion"></a>
The `version` of the runtime to use\. Currently, the only allowed version is `1.0.0`\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)