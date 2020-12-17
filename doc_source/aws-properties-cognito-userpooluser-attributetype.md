# AWS::Cognito::UserPoolUser AttributeType<a name="aws-properties-cognito-userpooluser-attributetype"></a>

Specifies whether the attribute is standard or custom\.

## Syntax<a name="aws-properties-cognito-userpooluser-attributetype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpooluser-attributetype-syntax.json"></a>

```
{
  "[Name](#cfn-cognito-userpooluser-attributetype-name)" : String,
  "[Value](#cfn-cognito-userpooluser-attributetype-value)" : String
}
```

### YAML<a name="aws-properties-cognito-userpooluser-attributetype-syntax.yaml"></a>

```
  [Name](#cfn-cognito-userpooluser-attributetype-name): String
  [Value](#cfn-cognito-userpooluser-attributetype-value): String
```

## Properties<a name="aws-properties-cognito-userpooluser-attributetype-properties"></a>

`Name`  <a name="cfn-cognito-userpooluser-attributetype-name"></a>
The name of the attribute\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Pattern*: `[\p{L}\p{M}\p{S}\p{N}\p{P}]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-cognito-userpooluser-attributetype-value"></a>
The value of the attribute\.  
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)