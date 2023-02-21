# AWS::CustomerProfiles::Integration SalesforceSourceProperties<a name="aws-properties-customerprofiles-integration-salesforcesourceproperties"></a>

The properties that are applied when Salesforce is being used as a source\.

## Syntax<a name="aws-properties-customerprofiles-integration-salesforcesourceproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-customerprofiles-integration-salesforcesourceproperties-syntax.json"></a>

```
{
  "[EnableDynamicFieldUpdate](#cfn-customerprofiles-integration-salesforcesourceproperties-enabledynamicfieldupdate)" : Boolean,
  "[IncludeDeletedRecords](#cfn-customerprofiles-integration-salesforcesourceproperties-includedeletedrecords)" : Boolean,
  "[Object](#cfn-customerprofiles-integration-salesforcesourceproperties-object)" : String
}
```

### YAML<a name="aws-properties-customerprofiles-integration-salesforcesourceproperties-syntax.yaml"></a>

```
  [EnableDynamicFieldUpdate](#cfn-customerprofiles-integration-salesforcesourceproperties-enabledynamicfieldupdate): Boolean
  [IncludeDeletedRecords](#cfn-customerprofiles-integration-salesforcesourceproperties-includedeletedrecords): Boolean
  [Object](#cfn-customerprofiles-integration-salesforcesourceproperties-object): String
```

## Properties<a name="aws-properties-customerprofiles-integration-salesforcesourceproperties-properties"></a>

`EnableDynamicFieldUpdate`  <a name="cfn-customerprofiles-integration-salesforcesourceproperties-enabledynamicfieldupdate"></a>
The flag that enables dynamic fetching of new \(recently added\) fields in the Salesforce objects while running a flow\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeDeletedRecords`  <a name="cfn-customerprofiles-integration-salesforcesourceproperties-includedeletedrecords"></a>
Indicates whether Amazon AppFlow includes deleted files in the flow run\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Object`  <a name="cfn-customerprofiles-integration-salesforcesourceproperties-object"></a>
The object specified in the Salesforce flow source\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)