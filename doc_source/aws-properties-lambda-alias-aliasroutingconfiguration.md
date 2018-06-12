# AWS Lambda Alias AliasRoutingConfiguration<a name="aws-properties-lambda-alias-aliasroutingconfiguration"></a>

<a name="aws-properties-lambda-alias-aliasroutingconfiguration-description"></a>The `AliasRoutingConfiguration` property type specifies two different versions of an AWS Lambda function, allowing you to dictate what percentage of traffic will invoke each version\. For more information, see [Routing Traffic to Different Function Versions Using Aliases](http://docs.aws.amazon.com/lambda/latest/dg/lambda-traffic-shifting-using-aliases.html) in the *AWS Lambda Developer Guide*\.

<a name="aws-properties-lambda-alias-aliasroutingconfiguration-inheritance"></a> `AliasRoutingConfiguration` is a property of the [AWS::Lambda::Alias](aws-resource-lambda-alias.md) resource type\.

## Syntax<a name="aws-properties-lambda-alias-aliasroutingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-alias-aliasroutingconfiguration-syntax.json"></a>

```
{
  "[AdditionalVersionWeights](#cfn-lambda-alias-aliasroutingconfiguration-additionalversionweights)" : [ [*VersionWeight*](aws-properties-lambda-alias-versionweight.md), ... ]
}
```

### YAML<a name="aws-properties-lambda-alias-aliasroutingconfiguration-syntax.yaml"></a>

```
[AdditionalVersionWeights](#cfn-lambda-alias-aliasroutingconfiguration-additionalversionweights): 
  - [*VersionWeight*](aws-properties-lambda-alias-versionweight.md)
```

## Properties<a name="aws-properties-lambda-alias-aliasroutingconfiguration-properties"></a>

`AdditionalVersionWeights`  <a name="cfn-lambda-alias-aliasroutingconfiguration-additionalversionweights"></a>
The percentage of traffic that will invoke the updated function version\.  
 *Required*: Yes  
 *Type*: List of [AWS Lambda Alias VersionWeight](aws-properties-lambda-alias-versionweight.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-lambda-alias-aliasroutingconfiguration-seealso"></a>
+ [Routing Traffic to Different Function Versions Using Aliases](http://docs.aws.amazon.com/lambda/latest/dg/lambda-traffic-shifting-using-aliases.html) in the *AWS Lambda Developer Guide*
+ [CreateAlias](http://docs.aws.amazon.com/lambda/latest/dg/API_CreateAlias.html) in the *AWS Lambda Developer Guide*
+ [AliasRoutingConfiguration](http://docs.aws.amazon.com/lambda/latest/dg/API_AliasRoutingConfiguration.html) in the *AWS Lambda Developer Guide*