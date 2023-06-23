# AWS::SecurityHub::AutomationRule SeverityUpdate<a name="aws-properties-securityhub-automationrule-severityupdate"></a>

Updates to the severity information for a finding\.

## Syntax<a name="aws-properties-securityhub-automationrule-severityupdate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-securityhub-automationrule-severityupdate-syntax.json"></a>

```
{
  "[Label](#cfn-securityhub-automationrule-severityupdate-label)" : String,
  "[Normalized](#cfn-securityhub-automationrule-severityupdate-normalized)" : Integer,
  "[Product](#cfn-securityhub-automationrule-severityupdate-product)" : Double
}
```

### YAML<a name="aws-properties-securityhub-automationrule-severityupdate-syntax.yaml"></a>

```
  [Label](#cfn-securityhub-automationrule-severityupdate-label): String
  [Normalized](#cfn-securityhub-automationrule-severityupdate-normalized): Integer
  [Product](#cfn-securityhub-automationrule-severityupdate-product): Double
```

## Properties<a name="aws-properties-securityhub-automationrule-severityupdate-properties"></a>

`Label`  <a name="cfn-securityhub-automationrule-severityupdate-label"></a>
The severity value of the finding\. The allowed values are the following\.  
+  `INFORMATIONAL` \- No issue was found\.
+  `LOW` \- The issue does not require action on its own\.
+  `MEDIUM` \- The issue must be addressed but not urgently\.
+  `HIGH` \- The issue must be addressed as a priority\.
+  `CRITICAL` \- The issue must be remediated immediately to avoid it escalating\.
*Required*: No  
*Type*: String  
*Allowed values*: `CRITICAL | HIGH | INFORMATIONAL | LOW | MEDIUM`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Normalized`  <a name="cfn-securityhub-automationrule-severityupdate-normalized"></a>
The normalized severity for the finding\. This attribute is to be deprecated in favor of `Label`\.  
If you provide `Normalized` and do not provide `Label`, `Label` is set automatically as follows\.  
+ 0 \- `INFORMATIONAL` 
+ 1–39 \- `LOW` 
+ 40–69 \- `MEDIUM` 
+ 70–89 \- `HIGH` 
+ 90–100 \- `CRITICAL` 
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Product`  <a name="cfn-securityhub-automationrule-severityupdate-product"></a>
The native severity as defined by the AWS service or integrated partner product that generated the finding\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)