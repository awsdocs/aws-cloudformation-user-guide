# AWS::VerifiedPermissions::Policy<a name="aws-resource-verifiedpermissions-policy"></a>

Creates or updates a Cedar policy and saves it in the specified policy store\. You can create either a static policy or a policy linked to a policy template\.

You can directly update only static policies\. To update a template\-linked policy, you must update it's linked policy template instead\.
+ To create a static policy, in the `Definition` include a `Static` element that includes the Cedar policy text in the `Statement` element\.
+ To create a policy that is dynamically linked to a policy template, in the `Definition` include a `Templatelinked` element that specifies the policy template ID and the principal and resource to associate with this policy\. If the policy template is ever updated, any policies linked to the policy template automatically use the updated template\.

**Note**  
If the policy store has validation enabled, then creating a policy causes it to be validated against the schema in the policy store\. If the policy doesn't pass validation, the operation fails and the policy isn't stored\.

## Syntax<a name="aws-resource-verifiedpermissions-policy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-verifiedpermissions-policy-syntax.json"></a>

```
{
  "Type" : "AWS::VerifiedPermissions::Policy",
  "Properties" : {
      "[Definition](#cfn-verifiedpermissions-policy-definition)" : PolicyDefinition,
      "[PolicyStoreId](#cfn-verifiedpermissions-policy-policystoreid)" : String
    }
}
```

### YAML<a name="aws-resource-verifiedpermissions-policy-syntax.yaml"></a>

```
Type: AWS::VerifiedPermissions::Policy
Properties: 
  [Definition](#cfn-verifiedpermissions-policy-definition): 
    PolicyDefinition
  [PolicyStoreId](#cfn-verifiedpermissions-policy-policystoreid): String
```

## Properties<a name="aws-resource-verifiedpermissions-policy-properties"></a>

`Definition`  <a name="cfn-verifiedpermissions-policy-definition"></a>
Specifies the policy type and content to use for the new or updated policy\. The definition structure must include either a `Static` or a `TemplateLinked` element\.  
*Required*: Yes  
*Type*: [PolicyDefinition](aws-properties-verifiedpermissions-policy-policydefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyStoreId`  <a name="cfn-verifiedpermissions-policy-policystoreid"></a>
Specifies the `PolicyStoreId` of the policy store you want to store the policy in\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-verifiedpermissions-policy-return-values"></a>

### Ref<a name="aws-resource-verifiedpermissions-policy-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the unique id of the new or updated policy\. For example:

`{ "Ref": "SPEXAMPLEabcdefg111111" }`

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-verifiedpermissions-policy-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-verifiedpermissions-policy-return-values-fn--getatt-fn--getatt"></a>

`PolicyId`  <a name="PolicyId-fn::getatt"></a>
The unique ID of the new or updated policy\.

`PolicyType`  <a name="PolicyType-fn::getatt"></a>
The type of the policy\. This is one of the following values:  
+ Static
+ TemplateLinked