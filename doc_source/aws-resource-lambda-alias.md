# AWS::Lambda::Alias<a name="aws-resource-lambda-alias"></a>

The `AWS::Lambda::Alias` resource creates an [alias](https://docs.aws.amazon.com/lambda/latest/dg/versioning-aliases.html) for a Lambda function version\. Use aliases to provide clients with a function identifier that you can update to invoke a different version\.

You can also map an alias to split invocation requests between two versions\. Use the `RoutingConfig` parameter to specify a second version and the percentage of invocation requests that it receives\.

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
      "[ProvisionedConcurrencyConfig](#cfn-lambda-alias-provisionedconcurrencyconfig)" : ProvisionedConcurrencyConfiguration,
      "[RoutingConfig](#cfn-lambda-alias-routingconfig)" : AliasRoutingConfiguration
    }
}
```

### YAML<a name="aws-resource-lambda-alias-syntax.yaml"></a>

```
Type: AWS::Lambda::Alias
Properties: 
  [Description](#cfn-lambda-alias-description): String
  [FunctionName](#cfn-lambda-alias-functionname): String
  [FunctionVersion](#cfn-lambda-alias-functionversion): String
  [Name](#cfn-lambda-alias-name): String
  [ProvisionedConcurrencyConfig](#cfn-lambda-alias-provisionedconcurrencyconfig): 
    ProvisionedConcurrencyConfiguration
  [RoutingConfig](#cfn-lambda-alias-routingconfig): 
    AliasRoutingConfiguration
```

## Properties<a name="aws-resource-lambda-alias-properties"></a>

`Description`  <a name="cfn-lambda-alias-description"></a>
A description of the alias\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FunctionName`  <a name="cfn-lambda-alias-functionname"></a>
The name of the Lambda function\.  

**Name formats**
+  **Function name** \- `MyFunction`\.
+  **Function ARN** \- `arn:aws:lambda:us-west-2:123456789012:function:MyFunction`\.
+  **Partial ARN** \- `123456789012:function:MyFunction`\.
The length constraint applies only to the full ARN\. If you specify only the function name, it is limited to 64 characters in length\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `140`  
*Pattern*: `(arn:(aws[a-zA-Z-]*)?:lambda:)?([a-z]{2}(-gov)?-[a-z]+-\d{1}:)?(\d{12}:)?(function:)?([a-zA-Z0-9-_]+)(:(\$LATEST|[a-zA-Z0-9-_]+))?`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FunctionVersion`  <a name="cfn-lambda-alias-functionversion"></a>
The function version that the alias invokes\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `(\$LATEST|[0-9]+)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-lambda-alias-name"></a>
The name of the alias\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `(?!^[0-9]+$)([a-zA-Z0-9-_]+)`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProvisionedConcurrencyConfig`  <a name="cfn-lambda-alias-provisionedconcurrencyconfig"></a>
Specifies a provisioned concurrency configuration for a function's alias\.  
*Required*: No  
*Type*: [ProvisionedConcurrencyConfiguration](aws-properties-lambda-alias-provisionedconcurrencyconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoutingConfig`  <a name="cfn-lambda-alias-routingconfig"></a>
The [routing configuration](https://docs.aws.amazon.com/lambda/latest/dg/lambda-traffic-shifting-using-aliases.html) of the alias\.  
*Required*: No  
*Type*: [AliasRoutingConfiguration](aws-properties-lambda-alias-aliasroutingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-lambda-alias-return-values"></a>

### Ref<a name="aws-resource-lambda-alias-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ARN\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-lambda-alias--examples"></a>



### Alias<a name="aws-resource-lambda-alias--examples--Alias"></a>

A Node\.js function with a version and alias\.

#### YAML<a name="aws-resource-lambda-alias--examples--Alias--yaml"></a>

```
Resources:
  function:
    Type: AWS::Lambda::Function
    Properties:
      Handler: index.handler
      Role: arn:aws:iam::123456789012:role/lambda-role
      Code:
        ZipFile: |
          exports.handler = function(event){
              console.log(JSON.stringify(event, null, 2))
              const response = {
                  statusCode: 200,
                  body: JSON.stringify('Hello from Lambda!')
              }
              return response
          };
      Runtime: nodejs12.x
      TracingConfig:
        Mode: Active
  version:
    Type: AWS::Lambda::Version
    Properties:
      FunctionName: !Ref function
      Description: v1
  alias:
    Type: AWS::Lambda::Alias
    Properties:
      FunctionName: !Ref function
      FunctionVersion: !GetAtt version.Version
      Name: BLUE
```

### Weighted Alias<a name="aws-resource-lambda-alias--examples--Weighted_Alias"></a>

An alias that routes requests to two versions\.

#### YAML<a name="aws-resource-lambda-alias--examples--Weighted_Alias--yaml"></a>

```
Resources:
  function:
    Type: AWS::Lambda::Function
    Properties:
      Handler: index.handler
      Role: arn:aws:iam::123456789012:role/lambda-role
      Code:
        ZipFile: |
          exports.handler = function(event){
              console.log(JSON.stringify(event, null, 2))
              const response = {
                  statusCode: 200,
                  body: JSON.stringify('Hello again from Lambda!')
              }
              return response
          }
      Runtime: nodejs12.x
      TracingConfig:
        Mode: Active
  version:
    Type: AWS::Lambda::Version
    Properties:
      FunctionName: !Ref function
      Description: v1
  newVersion:
    Type: AWS::Lambda::Version
    Properties:
      FunctionName: !Ref function
      Description: v2
  alias:
    Type: AWS::Lambda::Alias
    Properties:
      FunctionName: !Ref function
      FunctionVersion: !GetAtt newVersion.Version
      Name: BLUE
      RoutingConfig:
        AdditionalVersionWeights:
          - FunctionVersion: !GetAtt version.Version
            FunctionWeight: 0.5
```