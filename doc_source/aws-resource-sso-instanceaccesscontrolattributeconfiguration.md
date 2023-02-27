# AWS::SSO::InstanceAccessControlAttributeConfiguration<a name="aws-resource-sso-instanceaccesscontrolattributeconfiguration"></a>

Enables the attribute\-based access control \(ABAC\) feature for the specified IAM Identity Center instance\. You can also specify new attributes to add to your ABAC configuration during the enabling process\. For more information about ABAC, see [Attribute\-Based Access Control](https://docs.aws.amazon.com/singlesignon/latest/userguide/abac.html) in the *IAM Identity Center User Guide*\.

**Note**  
The `InstanceAccessControlAttributeConfiguration` property has been deprecated but is still supported for backwards compatibility purposes\. We recommend that you use the `AccessControlAttributes` property instead\.

## Syntax<a name="aws-resource-sso-instanceaccesscontrolattributeconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sso-instanceaccesscontrolattributeconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::SSO::InstanceAccessControlAttributeConfiguration",
  "Properties" : {
      "[AccessControlAttributes](#cfn-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattributes)" : [ AccessControlAttribute, ... ],
      "[InstanceArn](#cfn-sso-instanceaccesscontrolattributeconfiguration-instancearn)" : String
    }
}
```

### YAML<a name="aws-resource-sso-instanceaccesscontrolattributeconfiguration-syntax.yaml"></a>

```
Type: AWS::SSO::InstanceAccessControlAttributeConfiguration
Properties: 
  [AccessControlAttributes](#cfn-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattributes): 
    - AccessControlAttribute
  [InstanceArn](#cfn-sso-instanceaccesscontrolattributeconfiguration-instancearn): String
```

## Properties<a name="aws-resource-sso-instanceaccesscontrolattributeconfiguration-properties"></a>

`AccessControlAttributes`  <a name="cfn-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattributes"></a>
Lists the attributes that are configured for ABAC in the specified IAM Identity Center instance\.  
*Required*: No  
*Type*: List of [AccessControlAttribute](aws-properties-sso-instanceaccesscontrolattributeconfiguration-accesscontrolattribute.md)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceArn`  <a name="cfn-sso-instanceaccesscontrolattributeconfiguration-instancearn"></a>
The ARN of the IAM Identity Center instance under which the operation will be executed\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `10`  
*Maximum*: `1224`  
*Pattern*: `arn:(aws|aws-us-gov|aws-cn|aws-iso|aws-iso-b):sso:::instance/(sso)?ins-[a-zA-Z0-9-.]{16}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-sso-instanceaccesscontrolattributeconfiguration-return-values"></a>

### Ref<a name="aws-resource-sso-instanceaccesscontrolattributeconfiguration-return-values-ref"></a>

Specifies the IAM Identity Center identity store attributes to add to your ABAC configuration\. When using an external identity provider as an identity source, you can pass attributes through the SAML assertion\. Doing so provides an alternative to configuring attributes from the IAM Identity Center identity store\. If a SAML assertion passes any of these attributes, IAM Identity Center will replace the attribute value with the value from the IAM Identity Center identity store\.

## Examples<a name="aws-resource-sso-instanceaccesscontrolattributeconfiguration--examples"></a>



### Enabling and configuring attributes used for access control in IAM Identity Center<a name="aws-resource-sso-instanceaccesscontrolattributeconfiguration--examples--Enabling_and_configuring_attributes_used_for_access_control_in_"></a>

The following example enables ABAC in IAM Identity Center and creates a new attribute key `CostCenter` that is mapped to the Value `“${path:enterprise.costCenter}”` which is coming from your identity source\.

#### JSON<a name="aws-resource-sso-instanceaccesscontrolattributeconfiguration--examples--Enabling_and_configuring_attributes_used_for_access_control_in_--json"></a>

```
{
    "Resources": {
        "ABAC": {
            "Type": "AWS::SSO::InstanceAccessControlAttributeConfiguration",
            "Properties": {
                "InstanceArn": "arn:aws:sso:::instance/ssoins-instanceId",
                "AccessControlAttributes": [
                    {
                        "Key": "CostCenter",
                        "Value": {
                            "Source": [
                                "${path:enterprise.costCenter}"
                            ]
                        }
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-sso-instanceaccesscontrolattributeconfiguration--examples--Enabling_and_configuring_attributes_used_for_access_control_in_--yaml"></a>

```
Resources:
  ABAC:
    Type: 'AWS::SSO::InstanceAccessControlAttributeConfiguration'
    Properties:
      InstanceArn: 'arn:aws:sso:::instance/ssoins-instanceId'
      AccessControlAttributes:
        - Key: CostCenter
          Value:
            Source:
              - '${path:enterprise.costCenter}'
```