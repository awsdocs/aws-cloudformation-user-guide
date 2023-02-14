# AWS::Lambda::Url<a name="aws-resource-lambda-url"></a>

The `AWS::Lambda::Url` resource creates a function URL with the specified configuration parameters\. A [function URL](https://docs.aws.amazon.com/lambda/latest/dg/lambda-urls.html) is a dedicated HTTP\(S\) endpoint that you can use to invoke your function\.

## Syntax<a name="aws-resource-lambda-url-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lambda-url-syntax.json"></a>

```
{
  "Type" : "AWS::Lambda::Url",
  "Properties" : {
      "[AuthType](#cfn-lambda-url-authtype)" : String,
      "[Cors](#cfn-lambda-url-cors)" : Cors,
      "[InvokeMode](#cfn-lambda-url-invokemode)" : String,
      "[Qualifier](#cfn-lambda-url-qualifier)" : String,
      "[TargetFunctionArn](#cfn-lambda-url-targetfunctionarn)" : String
    }
}
```

### YAML<a name="aws-resource-lambda-url-syntax.yaml"></a>

```
Type: AWS::Lambda::Url
Properties: 
  [AuthType](#cfn-lambda-url-authtype): String
  [Cors](#cfn-lambda-url-cors): 
    Cors
  [InvokeMode](#cfn-lambda-url-invokemode): String
  [Qualifier](#cfn-lambda-url-qualifier): String
  [TargetFunctionArn](#cfn-lambda-url-targetfunctionarn): String
```

## Properties<a name="aws-resource-lambda-url-properties"></a>

`AuthType`  <a name="cfn-lambda-url-authtype"></a>
The type of authentication that your function URL uses\. Set to `AWS_IAM` if you want to restrict access to authenticated users only\. Set to `NONE` if you want to bypass IAM authentication to create a public endpoint\. For more information, see [Security and auth model for Lambda function URLs](https://docs.aws.amazon.com/lambda/latest/dg/urls-auth.html)\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `AWS_IAM | NONE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Cors`  <a name="cfn-lambda-url-cors"></a>
The [Cross\-Origin Resource Sharing \(CORS\)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) settings for your function URL\.  
*Required*: No  
*Type*: [Cors](aws-properties-lambda-url-cors.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InvokeMode`  <a name="cfn-lambda-url-invokemode"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Qualifier`  <a name="cfn-lambda-url-qualifier"></a>
The alias name\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TargetFunctionArn`  <a name="cfn-lambda-url-targetfunctionarn"></a>
The name of the Lambda function\.  

**Name formats**
+ **Function name** \- `my-function`\.
+ **Function ARN** \- `arn:aws:lambda:us-west-2:123456789012:function:my-function`\.
+ **Partial ARN** \- `123456789012:function:my-function`\.
The length constraint applies only to the full ARN\. If you specify only the function name, it is limited to 64 characters in length\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-lambda-url-return-values"></a>

### Ref<a name="aws-resource-lambda-url-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-lambda-url-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-lambda-url-return-values-fn--getatt-fn--getatt"></a>

`FunctionArn`  <a name="FunctionArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the function\.

`FunctionUrl`  <a name="FunctionUrl-fn::getatt"></a>
The HTTP URL endpoint for your function\.