# AWS::CodePipeline::CustomActionType ConfigurationProperties<a name="aws-properties-codepipeline-customactiontype-configurationproperties"></a>

The configuration properties for the custom action\.

**Note**  
You can refer to a name in the configuration properties of the custom action within the URL templates by following the format of \{Config:name\}, as long as the configuration property is both required and not secret\. For more information, see [Create a Custom Action for a Pipeline](https://docs.aws.amazon.com/codepipeline/latest/userguide/how-to-create-custom-action.html)\.

## Syntax<a name="aws-properties-codepipeline-customactiontype-configurationproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codepipeline-customactiontype-configurationproperties-syntax.json"></a>

```
{
  "[Description](#cfn-codepipeline-customactiontype-configurationproperties-description)" : String,
  "[Key](#cfn-codepipeline-customactiontype-configurationproperties-key)" : Boolean,
  "[Name](#cfn-codepipeline-customactiontype-configurationproperties-name)" : String,
  "[Queryable](#cfn-codepipeline-customactiontype-configurationproperties-queryable)" : Boolean,
  "[Required](#cfn-codepipeline-customactiontype-configurationproperties-required)" : Boolean,
  "[Secret](#cfn-codepipeline-customactiontype-configurationproperties-secret)" : Boolean,
  "[Type](#cfn-codepipeline-customactiontype-configurationproperties-type)" : String
}
```

### YAML<a name="aws-properties-codepipeline-customactiontype-configurationproperties-syntax.yaml"></a>

```
  [Description](#cfn-codepipeline-customactiontype-configurationproperties-description): String
  [Key](#cfn-codepipeline-customactiontype-configurationproperties-key): Boolean
  [Name](#cfn-codepipeline-customactiontype-configurationproperties-name): String
  [Queryable](#cfn-codepipeline-customactiontype-configurationproperties-queryable): Boolean
  [Required](#cfn-codepipeline-customactiontype-configurationproperties-required): Boolean
  [Secret](#cfn-codepipeline-customactiontype-configurationproperties-secret): Boolean
  [Type](#cfn-codepipeline-customactiontype-configurationproperties-type): String
```

## Properties<a name="aws-properties-codepipeline-customactiontype-configurationproperties-properties"></a>

`Description`  <a name="cfn-codepipeline-customactiontype-configurationproperties-description"></a>
The description of the action configuration property that is displayed to users\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `160`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Key`  <a name="cfn-codepipeline-customactiontype-configurationproperties-key"></a>
Whether the configuration property is a key\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-codepipeline-customactiontype-configurationproperties-name"></a>
The name of the action configuration property\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Queryable`  <a name="cfn-codepipeline-customactiontype-configurationproperties-queryable"></a>
Indicates that the property is used with `PollForJobs`\. When creating a custom action, an action can have up to one queryable property\. If it has one, that property must be both required and not secret\.  
If you create a pipeline with a custom action type, and that custom action contains a queryable property, the value for that configuration property is subject to other restrictions\. The value must be less than or equal to twenty \(20\) characters\. The value can contain only alphanumeric characters, underscores, and hyphens\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Required`  <a name="cfn-codepipeline-customactiontype-configurationproperties-required"></a>
Whether the configuration property is a required value\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Secret`  <a name="cfn-codepipeline-customactiontype-configurationproperties-secret"></a>
Whether the configuration property is secret\. Secrets are hidden from all calls except for `GetJobDetails`, `GetThirdPartyJobDetails`, `PollForJobs`, and `PollForThirdPartyJobs`\.  
When updating a pipeline, passing \* \* \* \* \* without changing any other values of the action preserves the previous value of the secret\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-codepipeline-customactiontype-configurationproperties-type"></a>
The type of the configuration property\.  
*Required*: No  
*Type*: String  
*Allowed values*: `Boolean | Number | String`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)