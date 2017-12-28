# AWS CodePipeline CustomActionType ConfigurationProperties<a name="aws-resource-codepipeline-customactiontype-configurationproperties"></a>

`ConfigurationProperties` is a property of the [AWS::CodePipeline::CustomActionType](aws-resource-codepipeline-customactiontype.md) resource that defines a configuration for an AWS CodePipeline custom action\.

## Syntax<a name="w3ab2c21c14d366b5"></a>

### JSON<a name="aws-properties-codepipeline-customactiontype-configurationproperties-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-configurationproperties-description)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-configurationproperties-key)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-configurationproperties-name)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-configurationproperties-queryable)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-configurationproperties-required)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-configurationproperties-secret)" : Boolean,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-configurationproperties-type)" : String
}
```

### YAML<a name="aws-properties-codepipeline-customactiontype-configurationproperties-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-configurationproperties-description): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-configurationproperties-key): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-configurationproperties-name): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-configurationproperties-queryable): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-configurationproperties-required): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-configurationproperties-secret): Boolean
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codepipeline-customactiontype-configurationproperties-type): String
```

## Properties<a name="w3ab2c21c14d366b7"></a>

`Description`  
A description of this configuration property that will be displayed to users\.  
*Required: *No  
*Type*: String

`Key`  
Indicates whether the configuration property is a key\.  
*Required: *Yes  
*Type*: Boolean

`Name`  
A name for this configuration property\.  
*Required: *Yes  
*Type*: String

`Queryable`  
Indicates whether the configuration property will be used with the `PollForJobs` call\. A custom action can have one queryable property\. The queryable property must be required \(see the `Required` property\) and must not be secret \(see the `Secret` property\)\. For more information, see the `queryable` contents for the [ActionConfigurationProperty](http://docs.aws.amazon.com/codepipeline/latest/APIReference/API_ActionConfigurationProperty.html) data type in the *AWS CodePipeline API Reference*\.  
*Required: *No  
*Type*: Boolean

`Required`  
Indicates whether the configuration property is a required value\.  
*Required: *Yes  
*Type*: Boolean

`Secret`  
Indicates whether the configuration property is secret\. Secret configuration properties are hidden from all AWS CodePipeline calls except for `GetJobDetails`, `GetThirdPartyJobDetails`, `PollForJobs`, and `PollForThirdPartyJobs`\.  
*Required: *Yes  
*Type*: Boolean

`Type`  
The type of the configuration property, such as `String`, `Number`, or `Boolean`\.  
*Required: *No  
*Type*: String