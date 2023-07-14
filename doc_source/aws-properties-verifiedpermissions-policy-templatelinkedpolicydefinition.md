# AWS::VerifiedPermissions::Policy TemplateLinkedPolicyDefinition<a name="aws-properties-verifiedpermissions-policy-templatelinkedpolicydefinition"></a>

A structure that describes a policy created by instantiating a policy template\.

**Note**  
You can't directly update a template\-linked policy\. You must update the associated policy template instead\.

## Syntax<a name="aws-properties-verifiedpermissions-policy-templatelinkedpolicydefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-verifiedpermissions-policy-templatelinkedpolicydefinition-syntax.json"></a>

```
{
  "[PolicyTemplateId](#cfn-verifiedpermissions-policy-templatelinkedpolicydefinition-policytemplateid)" : String,
  "[Principal](#cfn-verifiedpermissions-policy-templatelinkedpolicydefinition-principal)" : EntityIdentifier,
  "[Resource](#cfn-verifiedpermissions-policy-templatelinkedpolicydefinition-resource)" : EntityIdentifier
}
```

### YAML<a name="aws-properties-verifiedpermissions-policy-templatelinkedpolicydefinition-syntax.yaml"></a>

```
  [PolicyTemplateId](#cfn-verifiedpermissions-policy-templatelinkedpolicydefinition-policytemplateid): String
  [Principal](#cfn-verifiedpermissions-policy-templatelinkedpolicydefinition-principal): 
    EntityIdentifier
  [Resource](#cfn-verifiedpermissions-policy-templatelinkedpolicydefinition-resource): 
    EntityIdentifier
```

## Properties<a name="aws-properties-verifiedpermissions-policy-templatelinkedpolicydefinition-properties"></a>

`PolicyTemplateId`  <a name="cfn-verifiedpermissions-policy-templatelinkedpolicydefinition-policytemplateid"></a>
The unique identifier of the policy template used to create this policy\.  
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`Principal`  <a name="cfn-verifiedpermissions-policy-templatelinkedpolicydefinition-principal"></a>
The principal associated with this template\-linked policy\. Verified Permissions substitutes this principal for the `?principal` placeholder in the policy template when it evaluates an authorization request\.  
*Required*: No  
*Type*: [EntityIdentifier](aws-properties-verifiedpermissions-policy-entityidentifier.md)  
*Update requires*: Updates are not supported\.

`Resource`  <a name="cfn-verifiedpermissions-policy-templatelinkedpolicydefinition-resource"></a>
The resource associated with this template\-linked policy\. Verified Permissions substitutes this resource for the `?resource` placeholder in the policy template when it evaluates an authorization request\.  
*Required*: No  
*Type*: [EntityIdentifier](aws-properties-verifiedpermissions-policy-entityidentifier.md)  
*Update requires*: Updates are not supported\.