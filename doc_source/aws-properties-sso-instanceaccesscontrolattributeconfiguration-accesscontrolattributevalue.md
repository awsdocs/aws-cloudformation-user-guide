# AWS::SSO::InstanceAccessControlAttributeConfiguration AccessControlAttributeValue<a name="aws-properties-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattributevalue"></a>

The value used for mapping a specified attribute to an identity source\.

## Syntax<a name="aws-properties-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattributevalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattributevalue-syntax.json"></a>

```
{
  "[Source](#cfn-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattributevalue-source)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattributevalue-syntax.yaml"></a>

```
  [Source](#cfn-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattributevalue-source): 
    - String
```

## Properties<a name="aws-properties-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattributevalue-properties"></a>

`Source`  <a name="cfn-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattributevalue-source"></a>
The identity source to use when mapping a specified attribute to IAM Identity Center\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)