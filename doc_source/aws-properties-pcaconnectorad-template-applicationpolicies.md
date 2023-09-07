# AWS::PCAConnectorAD::Template ApplicationPolicies<a name="aws-properties-pcaconnectorad-template-applicationpolicies"></a>

Application policies describe what the certificate can be used for\.

## Syntax<a name="aws-properties-pcaconnectorad-template-applicationpolicies-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pcaconnectorad-template-applicationpolicies-syntax.json"></a>

```
{
  "[Critical](#cfn-pcaconnectorad-template-applicationpolicies-critical)" : Boolean,
  "[Policies](#cfn-pcaconnectorad-template-applicationpolicies-policies)" : [ ApplicationPolicy, ... ]
}
```

### YAML<a name="aws-properties-pcaconnectorad-template-applicationpolicies-syntax.yaml"></a>

```
  [Critical](#cfn-pcaconnectorad-template-applicationpolicies-critical): Boolean
  [Policies](#cfn-pcaconnectorad-template-applicationpolicies-policies): 
    - ApplicationPolicy
```

## Properties<a name="aws-properties-pcaconnectorad-template-applicationpolicies-properties"></a>

`Critical`  <a name="cfn-pcaconnectorad-template-applicationpolicies-critical"></a>
Marks the application policy extension as critical\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Policies`  <a name="cfn-pcaconnectorad-template-applicationpolicies-policies"></a>
Application policies describe what the certificate can be used for\.  
*Required*: Yes  
*Type*: List of [ApplicationPolicy](aws-properties-pcaconnectorad-template-applicationpolicy.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)