# AWS::SecurityHub::AutomationRule WorkflowUpdate<a name="aws-properties-securityhub-automationrule-workflowupdate"></a>

Used to update information about the investigation into the finding\.

## Syntax<a name="aws-properties-securityhub-automationrule-workflowupdate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-securityhub-automationrule-workflowupdate-syntax.json"></a>

```
{
  "[Status](#cfn-securityhub-automationrule-workflowupdate-status)" : String
}
```

### YAML<a name="aws-properties-securityhub-automationrule-workflowupdate-syntax.yaml"></a>

```
  [Status](#cfn-securityhub-automationrule-workflowupdate-status): String
```

## Properties<a name="aws-properties-securityhub-automationrule-workflowupdate-properties"></a>

`Status`  <a name="cfn-securityhub-automationrule-workflowupdate-status"></a>
The status of the investigation into the finding\. The workflow status is specific to an individual finding\. It does not affect the generation of new findings\. For example, setting the workflow status to `SUPPRESSED` or `RESOLVED` does not prevent a new finding for the same issue\.  
The allowed values are the following\.  
+  `NEW` \- The initial state of a finding, before it is reviewed\.

  Security Hub also resets `WorkFlowStatus` from `NOTIFIED` or `RESOLVED` to `NEW` in the following cases:
  + The record state changes from `ARCHIVED` to `ACTIVE`\.
  + The compliance status changes from `PASSED` to either `WARNING`, `FAILED`, or `NOT_AVAILABLE`\.
+  `NOTIFIED` \- Indicates that you notified the resource owner about the security issue\. Used when the initial reviewer is not the resource owner, and needs intervention from the resource owner\.
+  `RESOLVED` \- The finding was reviewed and remediated and is now considered resolved\.
+  `SUPPRESSED` \- Indicates that you reviewed the finding and do not believe that any action is needed\. The finding is no longer updated\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `NEW | NOTIFIED | RESOLVED | SUPPRESSED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)