# AWS::CustomerProfiles::Integration ZendeskSourceProperties<a name="aws-properties-customerprofiles-integration-zendesksourceproperties"></a>

The properties that are applied when using Zendesk as a flow source\.

## Syntax<a name="aws-properties-customerprofiles-integration-zendesksourceproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-customerprofiles-integration-zendesksourceproperties-syntax.json"></a>

```
{
  "[Object](#cfn-customerprofiles-integration-zendesksourceproperties-object)" : String
}
```

### YAML<a name="aws-properties-customerprofiles-integration-zendesksourceproperties-syntax.yaml"></a>

```
  [Object](#cfn-customerprofiles-integration-zendesksourceproperties-object): String
```

## Properties<a name="aws-properties-customerprofiles-integration-zendesksourceproperties-properties"></a>

`Object`  <a name="cfn-customerprofiles-integration-zendesksourceproperties-object"></a>
The object specified in the Zendesk flow source\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)