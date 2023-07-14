# AWS::VerifiedPermissions::Policy PolicyDefinition<a name="aws-properties-verifiedpermissions-policy-policydefinition"></a>

A structure that defines a Cedar policy\. It includes the policy type, a description, and a policy body\. This is a top level data type used to create a policy\.

This data type is used as a request parameter for the [CreatePolicy](https://docs.aws.amazon.com/verifiedpermissions/latest/apireference/API_CreatePolicy.html) operation\. This structure must always have either an `Static` or a `TemplateLinked` element\.

## Syntax<a name="aws-properties-verifiedpermissions-policy-policydefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-verifiedpermissions-policy-policydefinition-syntax.json"></a>

```
{
  "[Static](#cfn-verifiedpermissions-policy-policydefinition-static)" : StaticPolicyDefinition,
  "[TemplateLinked](#cfn-verifiedpermissions-policy-policydefinition-templatelinked)" : TemplateLinkedPolicyDefinition
}
```

### YAML<a name="aws-properties-verifiedpermissions-policy-policydefinition-syntax.yaml"></a>

```
  [Static](#cfn-verifiedpermissions-policy-policydefinition-static): 
    StaticPolicyDefinition
  [TemplateLinked](#cfn-verifiedpermissions-policy-policydefinition-templatelinked): 
    TemplateLinkedPolicyDefinition
```

## Properties<a name="aws-properties-verifiedpermissions-policy-policydefinition-properties"></a>

`Static`  <a name="cfn-verifiedpermissions-policy-policydefinition-static"></a>
A structure that describes a static policy\. An static policy doesn't use a template or allow placeholders for entities\.  
*Required*: No  
*Type*: [StaticPolicyDefinition](aws-properties-verifiedpermissions-policy-staticpolicydefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateLinked`  <a name="cfn-verifiedpermissions-policy-policydefinition-templatelinked"></a>
A structure that describes a policy that was instantiated from a template\. The template can specify placeholders for `principal` and `resource`\. When you use [CreatePolicy](https://docs.aws.amazon.com/verifiedpermissions/latest/apireference/API_CreatePolicy.html) to create a policy from a template, you specify the exact principal and resource to use for the instantiated policy\.  
*Required*: No  
*Type*: [TemplateLinkedPolicyDefinition](aws-properties-verifiedpermissions-policy-templatelinkedpolicydefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)