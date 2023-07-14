# AWS::SecurityHub::AutomationRule NoteUpdate<a name="aws-properties-securityhub-automationrule-noteupdate"></a>

The updated note\.

## Syntax<a name="aws-properties-securityhub-automationrule-noteupdate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-securityhub-automationrule-noteupdate-syntax.json"></a>

```
{
  "[Text](#cfn-securityhub-automationrule-noteupdate-text)" : String,
  "[UpdatedBy](#cfn-securityhub-automationrule-noteupdate-updatedby)" : Json
}
```

### YAML<a name="aws-properties-securityhub-automationrule-noteupdate-syntax.yaml"></a>

```
  [Text](#cfn-securityhub-automationrule-noteupdate-text): String
  [UpdatedBy](#cfn-securityhub-automationrule-noteupdate-updatedby): Json
```

## Properties<a name="aws-properties-securityhub-automationrule-noteupdate-properties"></a>

`Text`  <a name="cfn-securityhub-automationrule-noteupdate-text"></a>
The updated note text\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UpdatedBy`  <a name="cfn-securityhub-automationrule-noteupdate-updatedby"></a>
The principal that updated the note\.  
*Required*: Yes  
*Type*: Json  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)