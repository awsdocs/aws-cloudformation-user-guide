# AWS::VerifiedPermissions::Policy StaticPolicyDefinition<a name="aws-properties-verifiedpermissions-policy-staticpolicydefinition"></a>

A structure that defines a static policy\.

## Syntax<a name="aws-properties-verifiedpermissions-policy-staticpolicydefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-verifiedpermissions-policy-staticpolicydefinition-syntax.json"></a>

```
{
  "[Description](#cfn-verifiedpermissions-policy-staticpolicydefinition-description)" : String,
  "[Statement](#cfn-verifiedpermissions-policy-staticpolicydefinition-statement)" : String
}
```

### YAML<a name="aws-properties-verifiedpermissions-policy-staticpolicydefinition-syntax.yaml"></a>

```
  [Description](#cfn-verifiedpermissions-policy-staticpolicydefinition-description): String
  [Statement](#cfn-verifiedpermissions-policy-staticpolicydefinition-statement): String
```

## Properties<a name="aws-properties-verifiedpermissions-policy-staticpolicydefinition-properties"></a>

`Description`  <a name="cfn-verifiedpermissions-policy-staticpolicydefinition-description"></a>
The description of the static policy\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Statement`  <a name="cfn-verifiedpermissions-policy-staticpolicydefinition-statement"></a>
The policy content of the static policy, written in the Cedar policy language\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)