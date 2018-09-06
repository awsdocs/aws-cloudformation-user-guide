# AWS CodePipeline CustomActionType ConfigurationProperties<a name="aws-resource-codepipeline-customactiontype-configurationproperties"></a>

`ConfigurationProperties` is a property of the [AWS::CodePipeline::CustomActionType](aws-resource-codepipeline-customactiontype.md) resource that defines a configuration for an AWS CodePipeline custom action\.

## Syntax<a name="w3ab2c21c14d440b5"></a>

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

## Properties<a name="w3ab2c21c14d440b7"></a>

`Description`  <a name="cfn-codepipeline-customactiontype-configurationproperties-description"></a>
A description of this configuration property that will be displayed to users\.  
*Required*: No  
*Type*: String

`Key`  <a name="cfn-codepipeline-customactiontype-configurationproperties-key"></a>
Indicates whether the configuration property is a key\.  
*Required*: Yes  
*Type*: Boolean

`Name`  <a name="cfn-codepipeline-customactiontype-configurationproperties-name"></a>
A name for this configuration property\.  
*Required*: Yes  
*Type*: String

`Queryable`  <a name="cfn-codepipeline-customactiontype-configurationproperties-queryable"></a>
Indicates whether the configuration property will be used with the `PollForJobs` call\. A custom action can have one queryable property\. The queryable property must be required \(see the `Required` property\) and must not be secret \(see the `Secret` property\)\. For more information, see the `queryable` contents for the [ActionConfigurationProperty](http://docs.aws.amazon.com/codepipeline/latest/APIReference/API_ActionConfigurationProperty.html) data type in the *AWS CodePipeline API Reference*\.  
*Required*: No  
*Type*: Boolean

`Required`  <a name="cfn-codepipeline-customactiontype-configurationproperties-required"></a>
Indicates whether the configuration property is a required value\.  
*Required*: Yes  
*Type*: Boolean

`Secret`  <a name="cfn-codepipeline-customactiontype-configurationproperties-secret"></a>
Indicates whether the configuration property is secret\. Secret configuration properties are hidden from all AWS CodePipeline calls except for `GetJobDetails`, `GetThirdPartyJobDetails`, `PollForJobs`, and `PollForThirdPartyJobs`\.  
*Required*: Yes  
*Type*: Boolean

`Type`  <a name="cfn-codepipeline-customactiontype-configurationproperties-type"></a>
The type of the configuration property, such as `String`, `Number`, or `Boolean`\.  
*Required*: No  
*Type*: String