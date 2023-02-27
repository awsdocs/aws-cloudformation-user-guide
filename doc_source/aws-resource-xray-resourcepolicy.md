# AWS::XRay::ResourcePolicy<a name="aws-resource-xray-resourcepolicy"></a>

 Sets the resource policy to grant one or more AWS services and accounts permissions to access X\-Ray\. Each resource policy will be associated with a specific AWS account\. Each AWS account can have a maximum of 5 resource policies, and each policy name must be unique within that account\. The maximum size of each resource policy is 5KB\. 

## Syntax<a name="aws-resource-xray-resourcepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-xray-resourcepolicy-syntax.json"></a>

```
{
  "Type" : "AWS::XRay::ResourcePolicy",
  "Properties" : {
      "[BypassPolicyLockoutCheck](#cfn-xray-resourcepolicy-bypasspolicylockoutcheck)" : Boolean,
      "[PolicyDocument](#cfn-xray-resourcepolicy-policydocument)" : String,
      "[PolicyName](#cfn-xray-resourcepolicy-policyname)" : String
    }
}
```

### YAML<a name="aws-resource-xray-resourcepolicy-syntax.yaml"></a>

```
Type: AWS::XRay::ResourcePolicy
Properties: 
  [BypassPolicyLockoutCheck](#cfn-xray-resourcepolicy-bypasspolicylockoutcheck): Boolean
  [PolicyDocument](#cfn-xray-resourcepolicy-policydocument): String
  [PolicyName](#cfn-xray-resourcepolicy-policyname): String
```

## Properties<a name="aws-resource-xray-resourcepolicy-properties"></a>

`BypassPolicyLockoutCheck`  <a name="cfn-xray-resourcepolicy-bypasspolicylockoutcheck"></a>
Property description not available\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyDocument`  <a name="cfn-xray-resourcepolicy-policydocument"></a>
The resource policy document, which can be up to 5kb in size\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyName`  <a name="cfn-xray-resourcepolicy-policyname"></a>
The name of the resource policy\. Must be unique within a specific AWS account\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\w+=,.@-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-xray-resourcepolicy-return-values"></a>

### Ref<a name="aws-resource-xray-resourcepolicy-return-values-ref"></a>