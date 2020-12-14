# AWS::FMS::Policy ResourceTag<a name="aws-properties-fms-policy-resourcetag"></a>

The resource tags that AWS Firewall Manager uses to determine if a particular resource should be included or excluded from the AWS Firewall Manager policy\. Tags enable you to categorize your AWS resources in different ways, for example, by purpose, owner, or environment\. Each tag consists of a key and an optional value\. Firewall Manager combines the tags with "AND" so that, if you add more than one tag to a policy scope, a resource must have all the specified tags to be included or excluded\. For more information, see [Working with Tag Editor](https://docs.aws.amazon.com/awsconsolehelpdocs/latest/gsg/tag-editor.html)\.

## Syntax<a name="aws-properties-fms-policy-resourcetag-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fms-policy-resourcetag-syntax.json"></a>

```
{
  "[Key](#cfn-fms-policy-resourcetag-key)" : String,
  "[Value](#cfn-fms-policy-resourcetag-value)" : String
}
```

### YAML<a name="aws-properties-fms-policy-resourcetag-syntax.yaml"></a>

```
  [Key](#cfn-fms-policy-resourcetag-key): String
  [Value](#cfn-fms-policy-resourcetag-value): String
```

## Properties<a name="aws-properties-fms-policy-resourcetag-properties"></a>

`Key`  <a name="cfn-fms-policy-resourcetag-key"></a>
The resource tag key\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^([\p{L}\p{Z}\p{N}_.:/=+\-@]*)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-fms-policy-resourcetag-value"></a>
The resource tag value\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `^([\p{L}\p{Z}\p{N}_.:/=+\-@]*)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)