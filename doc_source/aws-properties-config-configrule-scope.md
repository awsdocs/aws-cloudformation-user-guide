# AWS::Config::ConfigRule Scope<a name="aws-properties-config-configrule-scope"></a>

Defines which resources trigger an evaluation for an AWS Config rule\. The scope can include one or more resource types, a combination of a tag key and value, or a combination of one resource type and one resource ID\. Specify a scope to constrain which resources trigger an evaluation for a rule\. Otherwise, evaluations for the rule are triggered when any resource in your recording group changes in configuration\.

## Syntax<a name="aws-properties-config-configrule-scope-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-config-configrule-scope-syntax.json"></a>

```
{
  "[ComplianceResourceId](#cfn-config-configrule-scope-complianceresourceid)" : String,
  "[ComplianceResourceTypes](#cfn-config-configrule-scope-complianceresourcetypes)" : [ String, ... ],
  "[TagKey](#cfn-config-configrule-scope-tagkey)" : String,
  "[TagValue](#cfn-config-configrule-scope-tagvalue)" : String
}
```

### YAML<a name="aws-properties-config-configrule-scope-syntax.yaml"></a>

```
  [ComplianceResourceId](#cfn-config-configrule-scope-complianceresourceid): String
  [ComplianceResourceTypes](#cfn-config-configrule-scope-complianceresourcetypes): 
    - String
  [TagKey](#cfn-config-configrule-scope-tagkey): String
  [TagValue](#cfn-config-configrule-scope-tagvalue): String
```

## Properties<a name="aws-properties-config-configrule-scope-properties"></a>

`ComplianceResourceId`  <a name="cfn-config-configrule-scope-complianceresourceid"></a>
The ID of the only AWS resource that you want to trigger an evaluation for the rule\. If you specify a resource ID, you must specify one resource type for `ComplianceResourceTypes`\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `768`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComplianceResourceTypes`  <a name="cfn-config-configrule-scope-complianceresourcetypes"></a>
The resource types of only those AWS resources that you want to trigger an evaluation for the rule\. You can only specify one type if you also specify a resource ID for `ComplianceResourceId`\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TagKey`  <a name="cfn-config-configrule-scope-tagkey"></a>
The tag key that is applied to only those AWS resources that you want to trigger an evaluation for the rule\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TagValue`  <a name="cfn-config-configrule-scope-tagvalue"></a>
The tag value applied to only those AWS resources that you want to trigger an evaluation for the rule\. If you specify a value for `TagValue`, you must also specify a value for `TagKey`\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)