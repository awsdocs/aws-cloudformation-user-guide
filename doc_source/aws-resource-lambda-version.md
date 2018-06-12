# AWS::Lambda::Version<a name="aws-resource-lambda-version"></a>

The `AWS::Lambda::Version` resource publishes a specified version of an AWS Lambda \(Lambda\) function\. When publishing a new version of your function, Lambda copies the latest version of your function\. For more information, see [Introduction to AWS Lambda Versioning](http://docs.aws.amazon.com/lambda/latest/dg/versioning-intro.html) in the *AWS Lambda Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-lambda-version-syntax)
+ [Properties](#w3ab2c21c10d864b9)
+ [Return Values](#w3ab2c21c10d864c11)
+ [Example](#w3ab2c21c10d864c13)

## Syntax<a name="aws-resource-lambda-version-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lambda-version-syntax.json"></a>

```
{
  "Type" : "AWS::Lambda::Version",
  "Properties" : {    
    "[CodeSha256](#cfn-lambda-version-codesha256)" : String,
    "[Description](#cfn-lambda-version-description)" : String,         
    "[FunctionName](#cfn-lambda-version-functionname)" : String
  }
}
```

### YAML<a name="aws-resource-lambda-version-syntax.yaml"></a>

```
Type: "AWS::Lambda::Version"
Properties:     
  [CodeSha256](#cfn-lambda-version-codesha256) : String
  [Description](#cfn-lambda-version-description) : String         
  [FunctionName](#cfn-lambda-version-functionname) : String
```

## Properties<a name="w3ab2c21c10d864b9"></a>

`CodeSha256`  <a name="cfn-lambda-version-codesha256"></a>
The SHA\-256 hash of the deployment package that you want to publish\. This value must match the SHA\-256 hash of the `$LATEST` version of the function\. Specify this property to validate that you are publishing the correct package\.   
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.

`Description`  <a name="cfn-lambda-version-description"></a>
A description of the version you are publishing\. If you don't specify a value, Lambda copies the description from the `$LATEST` version of the function\.  
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.

`FunctionName`  <a name="cfn-lambda-version-functionname"></a>
The Lambda function for which you want to publish a version\. You can specify the function's name or its Amazon Resource Name \(ARN\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="w3ab2c21c10d864c11"></a>

### Ref<a name="w3ab2c21c10d864c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the ARN of the Lambda version, such as `arn:aws:lambda:us-west-2:123456789012:function:helloworld:1`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d864c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of the specified resource type\.

`Version`  
The published version of a Lambda version, such as `1`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Example<a name="w3ab2c21c10d864c13"></a>

The following example publishes a new version of the `MyFunction` Lambda function\.

### JSON<a name="aws-resource-lambda-version-example.json"></a>

```
"TestingNewFeature" : {
  "Type" : "AWS::Lambda::Version",
  "Properties" : {
    "FunctionName" : { "Ref" : "MyFunction" },
    "Description" : "A test version of MyFunction"
  }
}
```

### YAML<a name="aws-resource-lambda-version-example.yaml"></a>

```
TestingNewFeature: 
  Type: "AWS::Lambda::Version"
  Properties: 
    FunctionName: 
      Ref: "MyFunction"
    Description: "A test version of MyFunction"
```