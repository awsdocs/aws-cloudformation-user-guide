# AWS::Lambda::Version<a name="aws-resource-lambda-version"></a>

The `AWS::Lambda::Version` resource creates a [version](https://docs.aws.amazon.com/lambda/latest/dg/versioning-aliases.html) from the current code and configuration of a function\. Use versions to create a snapshot of your function code and configuration that doesn't change\.

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
Type: AWS::Lambda::Version
Properties:
  [CodeSha256](#cfn-lambda-version-codesha256): String
  [Description](#cfn-lambda-version-description): String
  [FunctionName](#cfn-lambda-version-functionname): String
```

## Properties<a name="aws-resource-lambda-version-properties"></a>

`CodeSha256`  <a name="cfn-lambda-version-codesha256"></a>
Only publish a version if the hash value matches the value that's specified\. Use this option to avoid publishing a version if the function code has changed since you last updated it\.
*Required*: No
*Type*: String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-lambda-version-description"></a>
A description for the version to override the description in the function configuration\.
*Required*: No
*Type*: String
*Minimum*: `0`
*Maximum*: `256`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FunctionName`  <a name="cfn-lambda-version-functionname"></a>
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

## Return Values<a name="aws-resource-lambda-version-return-values"></a>

### Ref<a name="aws-resource-lambda-version-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the version, such as `arn:aws:lambda:us-west-2:123456789012:function:helloworld:1`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-lambda-version-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-lambda-version-return-values-fn--getatt-fn--getatt"></a>

`Version`  <a name="Version-fn::getatt"></a>
The version number\.

## Examples<a name="aws-resource-lambda-version--examples"></a>

### Function Version<a name="aws-resource-lambda-version--examples--Function_Version"></a>

Create a version of function `MyFunction`\.

#### JSON<a name="aws-resource-lambda-version--examples--Function_Version--json"></a>

```
"MyVersion": {
    "Type": "AWS::Lambda::Version",
    "Properties": {
        "FunctionName": {
            "Ref": "MyFunction"
        },
        "Description": "A test version of MyFunction"
    }
}
```

#### YAML<a name="aws-resource-lambda-version--examples--Function_Version--yaml"></a>

```
MyVersion:
  Type: AWS::Lambda::Version
  Properties:
    FunctionName:
      Ref: "MyFunction"
    Description: "A test version of MyFunction"
```
