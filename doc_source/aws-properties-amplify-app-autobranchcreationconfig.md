# AWS::Amplify::App AutoBranchCreationConfig<a name="aws-properties-amplify-app-autobranchcreationconfig"></a>

 Use the AutoBranchCreationConfig property type to automatically create branches that match a certain pattern\. 

## Syntax<a name="aws-properties-amplify-app-autobranchcreationconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amplify-app-autobranchcreationconfig-syntax.json"></a>

```
{
  "[AutoBranchCreationPatterns](#cfn-amplify-app-autobranchcreationconfig-autobranchcreationpatterns)" : [ String, ... ],
  "[BasicAuthConfig](#cfn-amplify-app-autobranchcreationconfig-basicauthconfig)" : [BasicAuthConfig](aws-properties-amplify-app-basicauthconfig.md),
  "[BuildSpec](#cfn-amplify-app-autobranchcreationconfig-buildspec)" : String,
  "[EnableAutoBranchCreation](#cfn-amplify-app-autobranchcreationconfig-enableautobranchcreation)" : Boolean,
  "[EnableAutoBuild](#cfn-amplify-app-autobranchcreationconfig-enableautobuild)" : Boolean,
  "[EnvironmentVariables](#cfn-amplify-app-autobranchcreationconfig-environmentvariables)" : [ [EnvironmentVariable](aws-properties-amplify-app-environmentvariable.md), ... ],
  "[Stage](#cfn-amplify-app-autobranchcreationconfig-stage)" : String
}
```

### YAML<a name="aws-properties-amplify-app-autobranchcreationconfig-syntax.yaml"></a>

```
  [AutoBranchCreationPatterns](#cfn-amplify-app-autobranchcreationconfig-autobranchcreationpatterns): 
    - String
  [BasicAuthConfig](#cfn-amplify-app-autobranchcreationconfig-basicauthconfig): 
    [BasicAuthConfig](aws-properties-amplify-app-basicauthconfig.md)
  [BuildSpec](#cfn-amplify-app-autobranchcreationconfig-buildspec): String
  [EnableAutoBranchCreation](#cfn-amplify-app-autobranchcreationconfig-enableautobranchcreation): Boolean
  [EnableAutoBuild](#cfn-amplify-app-autobranchcreationconfig-enableautobuild): Boolean
  [EnvironmentVariables](#cfn-amplify-app-autobranchcreationconfig-environmentvariables): 
    - [EnvironmentVariable](aws-properties-amplify-app-environmentvariable.md)
  [Stage](#cfn-amplify-app-autobranchcreationconfig-stage): String
```

## Properties<a name="aws-properties-amplify-app-autobranchcreationconfig-properties"></a>

`AutoBranchCreationPatterns`  <a name="cfn-amplify-app-autobranchcreationconfig-autobranchcreationpatterns"></a>
Automated branch creation glob patterns for the Amplify app\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BasicAuthConfig`  <a name="cfn-amplify-app-autobranchcreationconfig-basicauthconfig"></a>
Sets password protection for your auto created branch\.  
*Required*: No  
*Type*: [BasicAuthConfig](aws-properties-amplify-app-basicauthconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BuildSpec`  <a name="cfn-amplify-app-autobranchcreationconfig-buildspec"></a>
Build spec for the auto created branch\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableAutoBranchCreation`  <a name="cfn-amplify-app-autobranchcreationconfig-enableautobranchcreation"></a>
Enables automated branch creation for the Amplify app\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableAutoBuild`  <a name="cfn-amplify-app-autobranchcreationconfig-enableautobuild"></a>
Enables auto building for the auto created branch\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnvironmentVariables`  <a name="cfn-amplify-app-autobranchcreationconfig-environmentvariables"></a>
Environment variables for the auto created branch\.  
*Required*: No  
*Type*: List of [EnvironmentVariable](aws-properties-amplify-app-environmentvariable.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Stage`  <a name="cfn-amplify-app-autobranchcreationconfig-stage"></a>
Stage for the auto created branch\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)