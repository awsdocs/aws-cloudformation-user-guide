# AWS::Lambda::Function ImageConfig<a name="aws-properties-lambda-function-imageconfig"></a>

Configuration values that override the container image Dockerfile settings\. See [Container settings](https://docs.aws.amazon.com/lambda/latest/dg/images-parms.html)\. 

## Syntax<a name="aws-properties-lambda-function-imageconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-function-imageconfig-syntax.json"></a>

```
{
  "[Command](#cfn-lambda-function-imageconfig-command)" : [ String, ... ],
  "[EntryPoint](#cfn-lambda-function-imageconfig-entrypoint)" : [ String, ... ],
  "[WorkingDirectory](#cfn-lambda-function-imageconfig-workingdirectory)" : String
}
```

### YAML<a name="aws-properties-lambda-function-imageconfig-syntax.yaml"></a>

```
  [Command](#cfn-lambda-function-imageconfig-command): 
    - String
  [EntryPoint](#cfn-lambda-function-imageconfig-entrypoint): 
    - String
  [WorkingDirectory](#cfn-lambda-function-imageconfig-workingdirectory): String
```

## Properties<a name="aws-properties-lambda-function-imageconfig-properties"></a>

`Command`  <a name="cfn-lambda-function-imageconfig-command"></a>
Specifies parameters that you want to pass in with ENTRYPOINT\.   
*Required*: No  
*Type*: List of String  
*Maximum*: `1500`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EntryPoint`  <a name="cfn-lambda-function-imageconfig-entrypoint"></a>
Specifies the entry point to their application, which is typically the location of the runtime executable\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `1500`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WorkingDirectory`  <a name="cfn-lambda-function-imageconfig-workingdirectory"></a>
Specifies the working directory\.  
*Required*: No  
*Type*: String  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)