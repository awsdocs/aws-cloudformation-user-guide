# AWS::VerifiedPermissions::PolicyTemplate<a name="aws-resource-verifiedpermissions-policytemplate"></a>

Creates a policy template\. A template can use placeholders for the principal and resource\. A template must be instantiated into a policy by associating it with specific principals and resources to use for the placeholders\. That instantiated policy can then be considered in authorization decisions\. The instantiated policy works identically to any other policy, except that it is dynamically linked to the template\. If the template changes, then any policies that are linked to that template are immediately updated as well\.

## Syntax<a name="aws-resource-verifiedpermissions-policytemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-verifiedpermissions-policytemplate-syntax.json"></a>

```
{
  "Type" : "AWS::VerifiedPermissions::PolicyTemplate",
  "Properties" : {
      "[Description](#cfn-verifiedpermissions-policytemplate-description)" : String,
      "[PolicyStoreId](#cfn-verifiedpermissions-policytemplate-policystoreid)" : String,
      "[Statement](#cfn-verifiedpermissions-policytemplate-statement)" : String
    }
}
```

### YAML<a name="aws-resource-verifiedpermissions-policytemplate-syntax.yaml"></a>

```
Type: AWS::VerifiedPermissions::PolicyTemplate
Properties: 
  [Description](#cfn-verifiedpermissions-policytemplate-description): String
  [PolicyStoreId](#cfn-verifiedpermissions-policytemplate-policystoreid): String
  [Statement](#cfn-verifiedpermissions-policytemplate-statement): String
```

## Properties<a name="aws-resource-verifiedpermissions-policytemplate-properties"></a>

`Description`  <a name="cfn-verifiedpermissions-policytemplate-description"></a>
The description to attach to the new or updated policy template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyStoreId`  <a name="cfn-verifiedpermissions-policytemplate-policystoreid"></a>
The unique identifier of the policy store that contains the template\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Statement`  <a name="cfn-verifiedpermissions-policytemplate-statement"></a>
Specifies the content that you want to use for the new policy template, written in the Cedar policy language\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-verifiedpermissions-policytemplate-return-values"></a>

### Ref<a name="aws-resource-verifiedpermissions-policytemplate-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the unique id of the policy store followed by '\|' and the unique id of the new or updated policy template\. For example:

`{ "Ref": "POLICYSTOREabcde111111|POLICYTEMPLATEab111111" }`

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-verifiedpermissions-policytemplate-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-verifiedpermissions-policytemplate-return-values-fn--getatt-fn--getatt"></a>

`PolicyTemplateId`  <a name="PolicyTemplateId-fn::getatt"></a>
The unique identifier of the new or modified policy template\.

## Examples<a name="aws-resource-verifiedpermissions-policytemplate--examples"></a>



### Creating a policy template<a name="aws-resource-verifiedpermissions-policytemplate--examples--Creating_a_policy_template"></a>

The following example creates a policy template with the specified statement\.

#### JSON<a name="aws-resource-verifiedpermissions-policytemplate--examples--Creating_a_policy_template--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "AWS CloudFormation sample template for creating a policy template for Verified Permissions.",
    "Parameters": {
        "PolicyStoreId": {
            "Type": "String"
        },
        "Description": {
            "Type": "String"
        },
        "Statement": {
            "Type": "String"
        }
    },
    "Resources": {
        "PolicyTemplate": {
            "Type": "AWS::VerifiedPermissions::PolicyTemplate",
            "Properties": {
                "PolicyStoreId": {
                    "Ref": "PolicyStoreId"
                },
                "Description": {
                    "Ref": "Description"
                },
                "Statement": {
                    "Ref": "Statement"
                }
            }
        }
    },
    "Outputs": {
        "PolicyTemplateId": {
            "Value": {
                "Fn::GetAtt": [
                    "PolicyTemplate",
                    "PolicyTemplateId"
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-verifiedpermissions-policytemplate--examples--Creating_a_policy_template--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: >-
  Description": "AWS CloudFormation sample template for creating a policy template for Verified Permissions." 
Parameters:
  PolicyStoreId:
    Type: String
  Description:
    Type: String
  Statement:
    Type: String
Resources:
  PolicyTemplate:
    Type: AWS::VerifiedPermissions::PolicyTemplate
    Properties:
      PolicyStoreId: !Ref PolicyStoreId
      Description: !Ref Description
      Statement: !Ref Statement
Outputs:
  PolicyTemplateId:
    Value: !GetAtt PolicyTemplate.PolicyTemplateId
```