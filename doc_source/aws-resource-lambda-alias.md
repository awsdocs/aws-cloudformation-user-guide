# AWS::Lambda::Alias<a name="aws-resource-lambda-alias"></a>

The `AWS::Lambda::Alias` resource creates an alias that points to the version of an AWS Lambda \(Lambda\) function that you specify\. Use aliases when you want to control which version of your function other services or applications invoke\. Those services or applications can use your function's alias so that they don't need to be updated whenever you release a new version of your function\. For more information, see [Introduction to AWS Lambda Aliases](http://docs.aws.amazon.com/lambda/latest/dg/aliases-intro.html) in the *AWS Lambda Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-lambda-alias-syntax)
+ [Properties](#w3ab2c21c10d851b9)
+ [Return Value](#w3ab2c21c10d851c11)
+ [Examples](#aws-resource-lambda-alias-examples)

## Syntax<a name="aws-resource-lambda-alias-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lambda-alias-syntax.json"></a>

```
{
  "Type" : "AWS::Lambda::Alias",
  "Properties" : { 
    "[Description](#cfn-lambda-alias-description)" : String,         
    "[FunctionName](#cfn-lambda-alias-functionname)" : String,
    "[FunctionVersion](#cfn-lambda-alias-functionversion)" : String,
    "[Name](#cfn-lambda-alias-name)" : String,
    "[RoutingConfig](#cfn-lambda-alias-routingconfig)" : [*AliasRoutingConfiguration*](aws-properties-lambda-alias-aliasroutingconfiguration.md)
  }
}
```

### YAML<a name="aws-resource-lambda-alias-syntax.yaml"></a>

```
Type: "AWS::Lambda::Alias"
Properties:     
  [Description](#cfn-lambda-alias-description): String         
  [FunctionName](#cfn-lambda-alias-functionname): String
  [FunctionVersion](#cfn-lambda-alias-functionversion): String
  [Name](#cfn-lambda-alias-name): String
  [RoutingConfig](#cfn-lambda-alias-routingconfig): 
    AliasRoutingConfiguration
```

## Properties<a name="w3ab2c21c10d851b9"></a>

`Description`  <a name="cfn-lambda-alias-description"></a>
Information about the alias, such as its purpose or the Lambda function that is associated with it\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`FunctionName`  <a name="cfn-lambda-alias-functionname"></a>
The Lambda function that you want to associate with this alias\. You can specify the function's name or its Amazon Resource Name \(ARN\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`FunctionVersion`  <a name="cfn-lambda-alias-functionversion"></a>
The version of the Lambda function that you want to associate with this alias\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Name`  <a name="cfn-lambda-alias-name"></a>
A name for the alias\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RoutingConfig`  <a name="cfn-lambda-alias-routingconfig"></a>
Use this parameter to point your alias to two different function versions, allowing you to dictate what percentage of traffic will invoke each version\. For more information, see [Routing Traffic to Different Function Versions Using Aliases](http://docs.aws.amazon.com/lambda/latest/dg/lambda-traffic-shifting-using-aliases.html) in the *AWS Lambda Developer Guide*\.  
 *Required*: No  
 *Type*: [AWS Lambda Alias AliasRoutingConfiguration](aws-properties-lambda-alias-aliasroutingconfiguration.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Value<a name="w3ab2c21c10d851c11"></a>

### Ref<a name="w3ab2c21c10d851c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the ARN of the Lambda alias\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="aws-resource-lambda-alias-examples"></a>

### Lambda Alias<a name="aws-resource-lambda-alias-example1"></a>

The following example creates an alias named `TestingForMyApp`\. The alias points to the `TestingNewFeature` version of the `MyFunction` Lambda function\.

#### JSON<a name="aws-resource-lambda-alias-example.json"></a>

```
"AliasForMyApp" : {
  "Type" : "AWS::Lambda::Alias",
  "Properties" : {
    "FunctionName" : { "Ref" : "MyFunction" },
    "FunctionVersion" : { "Fn::GetAtt" : [ "TestingNewFeature", "Version" ] },
    "Name" : "TestingForMyApp"
  }
}
```

#### YAML<a name="aws-resource-lambda-alias-example.yaml"></a>

```
AliasForMyApp: 
  Type: "AWS::Lambda::Alias"
  Properties: 
    FunctionName: 
      Ref: "MyFunction"
    FunctionVersion: 
      Fn::GetAtt: 
        - "TestingNewFeature"
        - "Version"
    Name: "TestingForMyApp"
```

### Lambda Alias Update Policy<a name="aws-resource-lambda-alias-example2"></a>

The following example defines an update policy for an alias\.

#### JSON<a name="aws-resource-lambda-alias-example2.json"></a>

```
"Alias": {
  "Type": "AWS::Lambda::Alias",
  "Properties": {
    "FunctionName": {
      "Ref": "LambdaFunction"
    },
    "FunctionVersion": {
      "Fn::GetAtt": [
        "FunctionVersionTwo",
        "Version"
      ]
    },
    "Name": "MyAlias"
  },
  "UpdatePolicy": {
    "CodeDeployLambdaAliasUpdate": {
      "ApplicationName": {
        "Ref": "CodeDeployApplication"
      },
      "DeploymentGroupName": {
        "Ref": "CodeDeployDeploymentGroup"
      },
      "BeforeAllowTrafficHook": {
        "Ref": "PreHookLambdaFunction"
      },
      "AfterAllowTrafficHook": {
        "Ref": "PreHookLambdaFunction"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-lambda-alias-example2.yaml"></a>

```
Alias:
  Type: 'AWS::Lambda::Alias'
  Properties:
    FunctionName: !Ref LambdaFunction
    FunctionVersion: !GetAtt FunctionVersionTwo.Version
    Name: MyAlias
  UpdatePolicy:
    CodeDeployLambdaAliasUpdate:
      ApplicationName: !Ref CodeDeployApplication
      DeploymentGroupName: !Ref CodeDeployDeploymentGroup
      BeforeAllowTrafficHook: !Ref PreHookLambdaFunction
      AfterAllowTrafficHook: !Ref PreHookLambdaFunction
```