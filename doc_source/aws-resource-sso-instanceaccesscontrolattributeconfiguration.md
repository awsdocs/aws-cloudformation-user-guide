# AWS::SSO::InstanceAccessControlAttributeConfiguration<a name="aws-resource-sso-instanceaccesscontrolattributeconfiguration"></a>

Enables the attribute\-based access control \(ABAC\) feature for the specified AWS SSO instance\. You can also specify new attributes to add to your ABAC configuration during the enabling process\. For more information about ABAC, see [Attribute\-Based Access Control](https://docs.aws.amazon.com/singlesignon/latest/userguide/abac.html) in the *AWS SSO User Guide*\.

## Syntax<a name="aws-resource-sso-instanceaccesscontrolattributeconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-sso-instanceaccesscontrolattributeconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::SSO::InstanceAccessControlAttributeConfiguration",
  "Properties" : {
      "[InstanceAccessControlAttributeConfiguration](#cfn-sso-instanceaccesscontrolattributeconfiguration-instanceaccesscontrolattributeconfiguration)" : Json,
      "[InstanceArn](#cfn-sso-instanceaccesscontrolattributeconfiguration-instancearn)" : String
    }
}
```

### YAML<a name="aws-resource-sso-instanceaccesscontrolattributeconfiguration-syntax.yaml"></a>

```
Type: AWS::SSO::InstanceAccessControlAttributeConfiguration
Properties: 
  [InstanceAccessControlAttributeConfiguration](#cfn-sso-instanceaccesscontrolattributeconfiguration-instanceaccesscontrolattributeconfiguration): Json
  [InstanceArn](#cfn-sso-instanceaccesscontrolattributeconfiguration-instancearn): String
```

## Properties<a name="aws-resource-sso-instanceaccesscontrolattributeconfiguration-properties"></a>

`InstanceAccessControlAttributeConfiguration`  <a name="cfn-sso-instanceaccesscontrolattributeconfiguration-instanceaccesscontrolattributeconfiguration"></a>
Specifies the attributes to add to your ABAC configuration\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceArn`  <a name="cfn-sso-instanceaccesscontrolattributeconfiguration-instancearn"></a>
The ARN of the AWS SSO instance under which the operation will be executed\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `10`  
*Maximum*: `1224`  
*Pattern*: `arn:aws:sso:::instance/(sso)?ins-[a-zA-Z0-9-.]{16}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-sso-instanceaccesscontrolattributeconfiguration-return-values"></a>

### Ref<a name="aws-resource-sso-instanceaccesscontrolattributeconfiguration-return-values-ref"></a>

Specifies the AWS SSO identity store attributes to add to your ABAC configuration\. When using an external identity provider as an identity source, you can pass attributes through the SAML assertion\. Doing so provides an alternative to configuring attributes from the AWS SSO identity store\. If a SAML assertion passes any of these attributes, AWS SSO will replace the attribute value with the value from the AWS SSO identity store\.

## Examples<a name="aws-resource-sso-instanceaccesscontrolattributeconfiguration--examples"></a>



### Enabling and configuring attributes used for access control in AWS SSO<a name="aws-resource-sso-instanceaccesscontrolattributeconfiguration--examples--Enabling_and_configuring_attributes_used_for_access_control_in_AWS_SSO"></a>

The following example enables ABAC in AWS SSO and creates a new attribute key `CostCenter` that is mapped to the Value `“${path:enterprise.costCenter}”` which is coming from your identity source\.

#### JSON<a name="aws-resource-sso-instanceaccesscontrolattributeconfiguration--examples--Enabling_and_configuring_attributes_used_for_access_control_in_AWS_SSO--json"></a>

```
{
    "Resources": {
        "ABAC": {
            "Type": "AWS::SSO::InstanceAccessControlAttributeConfiguration",
            "Properties": {
                "InstanceArn": "arn:aws:sso:::instance/ssoins-instanceId",
                "InstanceAccessControlAttributeConfiguration": {
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
}
```

#### YAML<a name="aws-resource-sso-instanceaccesscontrolattributeconfiguration--examples--Enabling_and_configuring_attributes_used_for_access_control_in_AWS_SSO--yaml"></a>

```
Resources:
  ABAC:
    Type: AWS::SSO::InstanceAccessControlAttributeConfiguration
    Properties:
      InstanceArn: 'arn:aws:sso:::instance/ssoins-instanceId'
      InstanceAccessControlAttributeConfiguration:
        AccessControlAttributes:
          - Key: 'CostCenter'
            Value:
              Source:
                - '${path:enterprise.costCenter}'
```