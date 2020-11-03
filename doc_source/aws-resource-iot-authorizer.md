# AWS::IoT::Authorizer<a name="aws-resource-iot-authorizer"></a>

Creates an authorizer\.

## Syntax<a name="aws-resource-iot-authorizer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-authorizer-syntax.json"></a>

```
{
  "Type" : "AWS::IoT::Authorizer",
  "Properties" : {
      "[AuthorizerFunctionArn](#cfn-iot-authorizer-authorizerfunctionarn)" : String,
      "[AuthorizerName](#cfn-iot-authorizer-authorizername)" : String,
      "[SigningDisabled](#cfn-iot-authorizer-signingdisabled)" : Boolean,
      "[Status](#cfn-iot-authorizer-status)" : String,
      "[Tags](#cfn-iot-authorizer-tags)" : Tags,
      "[TokenKeyName](#cfn-iot-authorizer-tokenkeyname)" : String,
      "[TokenSigningPublicKeys](#cfn-iot-authorizer-tokensigningpublickeys)" : TokenSigningPublicKeys
    }
}
```

### YAML<a name="aws-resource-iot-authorizer-syntax.yaml"></a>

```
Type: AWS::IoT::Authorizer
Properties: 
  [AuthorizerFunctionArn](#cfn-iot-authorizer-authorizerfunctionarn): String
  [AuthorizerName](#cfn-iot-authorizer-authorizername): String
  [SigningDisabled](#cfn-iot-authorizer-signingdisabled): Boolean
  [Status](#cfn-iot-authorizer-status): String
  [Tags](#cfn-iot-authorizer-tags): 
    Tags
  [TokenKeyName](#cfn-iot-authorizer-tokenkeyname): String
  [TokenSigningPublicKeys](#cfn-iot-authorizer-tokensigningpublickeys): 
    TokenSigningPublicKeys
```

## Properties<a name="aws-resource-iot-authorizer-properties"></a>

`AuthorizerFunctionArn`  <a name="cfn-iot-authorizer-authorizerfunctionarn"></a>
The authorizer's Lambda function ARN\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthorizerName`  <a name="cfn-iot-authorizer-authorizername"></a>
The authorizer name\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SigningDisabled`  <a name="cfn-iot-authorizer-signingdisabled"></a>
Whether or not signing is disabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Status`  <a name="cfn-iot-authorizer-status"></a>
The status of the authorizer\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iot-authorizer-tags"></a>
Metadata which can be used to manage the authorizer\.  
*Required*: No  
*Type*: [Tags](aws-properties-iot-authorizer-tags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TokenKeyName`  <a name="cfn-iot-authorizer-tokenkeyname"></a>
The key used to extract the token from the HTTP headers\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TokenSigningPublicKeys`  <a name="cfn-iot-authorizer-tokensigningpublickeys"></a>
The public keys used to validate the token signature returned by your custom authentication service\.  
*Required*: No  
*Type*: [TokenSigningPublicKeys](aws-properties-iot-authorizer-tokensigningpublickeys.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iot-authorizer-return-values"></a>

### Ref<a name="aws-resource-iot-authorizer-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the thing name\. For example:

 `{ "Ref": "MyTemplate" }` 

For a stack named MyStack, a value similar to the following is returned:

 `MyStack-MyTemplate-AB1CDEFGHIJK` 

### Fn::GetAtt<a name="aws-resource-iot-authorizer-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iot-authorizer-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the AWS IoT authorizer, such as `arn:aws:iot:us-east-2:123456789012:rule/MyIoTAuthorizer`\.