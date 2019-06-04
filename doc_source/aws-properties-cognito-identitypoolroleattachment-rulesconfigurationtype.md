# AWS::Cognito::IdentityPoolRoleAttachment RulesConfigurationType<a name="aws-properties-cognito-identitypoolroleattachment-rulesconfigurationtype"></a>

`RulesConfigurationType` is a subproperty of the [RoleMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cognito-identitypoolroleattachment-rolemapping.html) property that defines the rules to be used for mapping users to roles\.

## Syntax<a name="aws-properties-cognito-identitypoolroleattachment-rulesconfigurationtype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-identitypoolroleattachment-rulesconfigurationtype-syntax.json"></a>

```
{
  "[Rules](#cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-rules)" : [ [MappingRule](aws-properties-cognito-identitypoolroleattachment-mappingrule.md), ... ]
}
```

### YAML<a name="aws-properties-cognito-identitypoolroleattachment-rulesconfigurationtype-syntax.yaml"></a>

```
  [Rules](#cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-rules): 
    - [MappingRule](aws-properties-cognito-identitypoolroleattachment-mappingrule.md)
```

## Properties<a name="aws-properties-cognito-identitypoolroleattachment-rulesconfigurationtype-properties"></a>

`Rules`  <a name="cfn-cognito-identitypoolroleattachment-rulesconfigurationtype-rules"></a>
A list of rules\. You can specify up to 25 rules per identity provider\.  
*Required*: Yes  
*Type*: List of [MappingRule](aws-properties-cognito-identitypoolroleattachment-mappingrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)