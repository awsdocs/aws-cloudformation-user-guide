# AWS Lambda Alias VersionWeight<a name="aws-properties-lambda-alias-versionweight"></a>

<a name="aws-properties-lambda-alias-versionweight-description"></a>The `VersionWeight` property type specifies the percentages of traffic that will invoke each function versions for an AWS Lambda alias\. For more information, see [Routing Traffic to Different Function Versions Using Aliases](http://docs.aws.amazon.com/lambda/latest/dg/lambda-traffic-shifting-using-aliases.html) in the *AWS Lambda Developer Guide*\.

<a name="aws-properties-lambda-alias-versionweight-inheritance"></a> `VersionWeight` is a property of the [AWS::Lambda::Alias](aws-resource-lambda-alias.md) resource type\.

## Syntax<a name="aws-properties-lambda-alias-versionweight-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-alias-versionweight-syntax.json"></a>

```
{
  "[FunctionVersion](#cfn-lambda-alias-versionweight-functionversion)" : String,
  "[FunctionWeight](#cfn-lambda-alias-versionweight-functionweight)" : Double
}
```

### YAML<a name="aws-properties-lambda-alias-versionweight-syntax.yaml"></a>

```
[FunctionVersion](#cfn-lambda-alias-versionweight-functionversion): String
[FunctionWeight](#cfn-lambda-alias-versionweight-functionweight): Double
```

## Properties<a name="aws-properties-lambda-alias-versionweight-properties"></a>

`FunctionVersion`  <a name="cfn-lambda-alias-versionweight-functionversion"></a>
Function version to which the alias points\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`FunctionWeight`  <a name="cfn-lambda-alias-versionweight-functionweight"></a>
The percentage of traffic that will invoke the function version\.   
 *Required*: Yes  
 *Type*: Double  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-lambda-alias-versionweight-seealso"></a>
+ [Routing Traffic to Different Function Versions Using Aliases](http://docs.aws.amazon.com/lambda/latest/dg/lambda-traffic-shifting-using-aliases.html) in the *AWS Lambda Developer Guide*
+ [AliasRoutingConfiguration](http://docs.aws.amazon.com/lambda/latest/dg/API_AliasRoutingConfiguration.html) in the *AWS Lambda Developer Guide*