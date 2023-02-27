# AWS::IoT::RoleAlias<a name="aws-resource-iot-rolealias"></a>

Specifies a role alias\.

Requires permission to access the [CreateRoleAlias](https://docs.aws.amazon.com/service-authorization/latest/reference/list_awsiot.html#awsiot-actions-as-permissions) action\.

## Syntax<a name="aws-resource-iot-rolealias-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-rolealias-syntax.json"></a>

```
{
  "Type" : "AWS::IoT::RoleAlias",
  "Properties" : {
      "[CredentialDurationSeconds](#cfn-iot-rolealias-credentialdurationseconds)" : Integer,
      "[RoleAlias](#cfn-iot-rolealias-rolealias)" : String,
      "[RoleArn](#cfn-iot-rolealias-rolearn)" : String,
      "[Tags](#cfn-iot-rolealias-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iot-rolealias-syntax.yaml"></a>

```
Type: AWS::IoT::RoleAlias
Properties: 
  [CredentialDurationSeconds](#cfn-iot-rolealias-credentialdurationseconds): Integer
  [RoleAlias](#cfn-iot-rolealias-rolealias): String
  [RoleArn](#cfn-iot-rolealias-rolearn): String
  [Tags](#cfn-iot-rolealias-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iot-rolealias-properties"></a>

`CredentialDurationSeconds`  <a name="cfn-iot-rolealias-credentialdurationseconds"></a>
The number of seconds for which the credential is valid\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleAlias`  <a name="cfn-iot-rolealias-rolealias"></a>
The role alias\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-iot-rolealias-rolearn"></a>
The role ARN\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iot-rolealias-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iot-rolealias-return-values"></a>

### Ref<a name="aws-resource-iot-rolealias-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the role alias name\.

### Fn::GetAtt<a name="aws-resource-iot-rolealias-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iot-rolealias-return-values-fn--getatt-fn--getatt"></a>

`RoleAliasArn`  <a name="RoleAliasArn-fn::getatt"></a>
The role alias ARN\.