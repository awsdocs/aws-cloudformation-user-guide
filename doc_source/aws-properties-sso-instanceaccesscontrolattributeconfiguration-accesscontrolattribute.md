# AWS::SSO::InstanceAccessControlAttributeConfiguration AccessControlAttribute<a name="aws-properties-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattribute"></a>

These are IAM Identity Center identity store attributes that you can configure for use in attributes\-based access control \(ABAC\)\. You can create permissions policies that determine who can access your AWS resources based upon the configured attribute values\. When you enable ABAC and specify `AccessControlAttributes`, IAM Identity Center passes the attribute values of the authenticated user into IAM for use in policy evaluation\.

## Syntax<a name="aws-properties-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattribute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattribute-syntax.json"></a>

```
{
  "[Key](#cfn-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattribute-key)" : String,
  "[Value](#cfn-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattribute-value)" : AccessControlAttributeValue
}
```

### YAML<a name="aws-properties-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattribute-syntax.yaml"></a>

```
  [Key](#cfn-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattribute-key): String
  [Value](#cfn-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattribute-value): 
    AccessControlAttributeValue
```

## Properties<a name="aws-properties-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattribute-properties"></a>

`Key`  <a name="cfn-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattribute-key"></a>
The name of the attribute associated with your identities in your identity source\. This is used to map a specified attribute in your identity source with an attribute in IAM Identity Center\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\p{L}\p{Z}\p{N}_.:\/=+\-@]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattribute-value"></a>
The value used for mapping a specified attribute to an identity source\.  
*Required*: Yes  
*Type*: [AccessControlAttributeValue](aws-properties-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattributevalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)