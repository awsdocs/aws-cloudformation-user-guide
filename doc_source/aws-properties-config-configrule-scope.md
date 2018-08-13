# AWS Config ConfigRule Scope<a name="aws-properties-config-configrule-scope"></a>

`Scope` is a property of the [AWS::Config::ConfigRule](aws-resource-config-configrule.md) resource that specifies which AWS resources will trigger AWS Config to run an evaluation when their configurations change\. The scope can include one or more resource types, a tag key and value, or one resource type and one resource ID\. You cannot specify a tag\-key value and a resource ID or type\.

## Syntax<a name="w3ab2c21c14d526b5"></a>

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

## Properties<a name="w3ab2c21c14d526b7"></a>

`ComplianceResourceId`  <a name="cfn-config-configrule-scope-complianceresourceid"></a>
The ID of an AWS resource that you want AWS Config to evaluate against a rule\. If you specify an ID, you must also specify a resource type for the `ComplianceResourceTypes` property\.   
*Required*: No  
*Type*: String

`ComplianceResourceTypes`  <a name="cfn-config-configrule-scope-complianceresourcetypes"></a>
The types of AWS resources that you want AWS Config to evaluate against the rule\. If you specify the `ComplianceResourceId` property, specify only one resource type\. For more information, see [Supported Resources, Configuration Items, and Relationships](http://docs.aws.amazon.com/config/latest/developerguide/resource-config-reference.html)\.  
*Required*: Conditional\. If you specify a value for the `ComplianceResourceId` property, you must also specify this property\.  
*Type*: List of String values

`TagKey`  <a name="cfn-config-configrule-scope-tagkey"></a>
The tag key that is applied to the AWS resources that you want AWS Config to evaluate against the rule\.  
*Required*: Conditional\. If you specify a tag value, you must specify this property\.  
*Type*: String

`TagValue`  <a name="cfn-config-configrule-scope-tagvalue"></a>
The tag value that is applied to the AWS resources that you want AWS Config to evaluate against the rule\.  
*Required*: Conditional\. If you specify a tag key, you must specify this property\.  
*Type*: String