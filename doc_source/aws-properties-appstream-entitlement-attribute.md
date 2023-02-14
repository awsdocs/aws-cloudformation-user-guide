# AWS::AppStream::Entitlement Attribute<a name="aws-properties-appstream-entitlement-attribute"></a>

An attribute that belongs to an entitlement\. Application entitlements work by matching a supported SAML 2\.0 attribute name to a value when a user identity federates to an AppStream 2\.0 SAML application\.

## Syntax<a name="aws-properties-appstream-entitlement-attribute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appstream-entitlement-attribute-syntax.json"></a>

```
{
  "[Name](#cfn-appstream-entitlement-attribute-name)" : String,
  "[Value](#cfn-appstream-entitlement-attribute-value)" : String
}
```

### YAML<a name="aws-properties-appstream-entitlement-attribute-syntax.yaml"></a>

```
  [Name](#cfn-appstream-entitlement-attribute-name): String
  [Value](#cfn-appstream-entitlement-attribute-value): String
```

## Properties<a name="aws-properties-appstream-entitlement-attribute-properties"></a>

`Name`  <a name="cfn-appstream-entitlement-attribute-name"></a>
A supported AWS IAM SAML PrincipalTag attribute that is matched to a value when a user identity federates to an AppStream 2\.0 SAML application\.  
The following are supported values:  
+ roles 
+ department 
+ organization 
+ groups 
+ title 
+ costCenter 
+ userType
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-appstream-entitlement-attribute-value"></a>
A value that is matched to a supported SAML attribute name when a user identity federates to an AppStream 2\.0 SAML application\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)