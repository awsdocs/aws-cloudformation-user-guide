# AWS::SSO::InstanceAccessControlAttributeConfiguration AccessControlAttributeValueSourceList<a name="aws-properties-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattributevaluesourcelist"></a>

The list of values used for mapping a specified attribute to an identity source\.

## Syntax<a name="aws-properties-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattributevaluesourcelist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattributevaluesourcelist-syntax.json"></a>

```
{
  "[AccessControlAttributeValueSourceList](#cfn-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattributevaluesourcelist-accesscontrolattributevaluesourcelist)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattributevaluesourcelist-syntax.yaml"></a>

```
  [AccessControlAttributeValueSourceList](#cfn-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattributevaluesourcelist-accesscontrolattributevaluesourcelist): 
    - String
```

## Properties<a name="aws-properties-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattributevaluesourcelist-properties"></a>

`AccessControlAttributeValueSourceList`  <a name="cfn-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattributevaluesourcelist-accesscontrolattributevaluesourcelist"></a>
Lists the identity source to use when mapping a specified attribute to AWS SSO\.  
*Required*: No  
*Type*: [List](#aws-properties-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattributevaluesourcelist) of [String](#aws-properties-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattributevaluesourcelist)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)