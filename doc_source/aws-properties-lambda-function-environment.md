# AWS::Lambda::Function Environment<a name="aws-properties-lambda-function-environment"></a>

A function's environment variable settings\. You can use environment variables to adjust your function's behavior without updating code\. An environment variable is a pair of strings that are stored in a function's version\-specific configuration\.

## Syntax<a name="aws-properties-lambda-function-environment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-function-environment-syntax.json"></a>

```
{
  "[Variables](#cfn-lambda-function-environment-variables)" : {Key : Value, ...}
}
```

### YAML<a name="aws-properties-lambda-function-environment-syntax.yaml"></a>

```
  [Variables](#cfn-lambda-function-environment-variables): 
    Key : Value
```

## Properties<a name="aws-properties-lambda-function-environment-properties"></a>

`Variables`  <a name="cfn-lambda-function-environment-variables"></a>
Environment variable key\-value pairs\. For more information, see [Using Lambda environment variables](https://docs.aws.amazon.com/lambda/latest/dg/configuration-envvars.html)\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-lambda-function-environment--examples"></a>

### Environment Variables<a name="aws-properties-lambda-function-environment--examples--Environment_Variables"></a>

Add environment variables to a function\. Each variable is a key\-value pair\. This example specifies values for a `databaseName` and a `databaseUser`\.

#### YAML<a name="aws-properties-lambda-function-environment--examples--Environment_Variables--yaml"></a>

```
      Environment:
        Variables:
          databaseName: lambdadb
          databaseUser: admin
```