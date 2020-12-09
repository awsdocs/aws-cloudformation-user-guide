# AWS::Amplify::App<a name="aws-resource-amplify-app"></a>

 The AWS::Amplify::App resource creates Apps in the Amplify Console\. An App is a collection of branches\. 

## Syntax<a name="aws-resource-amplify-app-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-amplify-app-syntax.json"></a>

```
{
  "Type" : "AWS::Amplify::App",
  "Properties" : {
      "[AccessToken](#cfn-amplify-app-accesstoken)" : String,
      "[AutoBranchCreationConfig](#cfn-amplify-app-autobranchcreationconfig)" : AutoBranchCreationConfig,
      "[BasicAuthConfig](#cfn-amplify-app-basicauthconfig)" : BasicAuthConfig,
      "[BuildSpec](#cfn-amplify-app-buildspec)" : String,
      "[CustomHeaders](#cfn-amplify-app-customheaders)" : String,
      "[CustomRules](#cfn-amplify-app-customrules)" : [ CustomRule, ... ],
      "[Description](#cfn-amplify-app-description)" : String,
      "[EnableBranchAutoDeletion](#cfn-amplify-app-enablebranchautodeletion)" : Boolean,
      "[EnvironmentVariables](#cfn-amplify-app-environmentvariables)" : [ EnvironmentVariable, ... ],
      "[IAMServiceRole](#cfn-amplify-app-iamservicerole)" : String,
      "[Name](#cfn-amplify-app-name)" : String,
      "[OauthToken](#cfn-amplify-app-oauthtoken)" : String,
      "[Repository](#cfn-amplify-app-repository)" : String,
      "[Tags](#cfn-amplify-app-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-amplify-app-syntax.yaml"></a>

```
Type: AWS::Amplify::App
Properties: 
  [AccessToken](#cfn-amplify-app-accesstoken): String
  [AutoBranchCreationConfig](#cfn-amplify-app-autobranchcreationconfig): 
    AutoBranchCreationConfig
  [BasicAuthConfig](#cfn-amplify-app-basicauthconfig): 
    BasicAuthConfig
  [BuildSpec](#cfn-amplify-app-buildspec): String
  [CustomHeaders](#cfn-amplify-app-customheaders): String
  [CustomRules](#cfn-amplify-app-customrules): 
    - CustomRule
  [Description](#cfn-amplify-app-description): String
  [EnableBranchAutoDeletion](#cfn-amplify-app-enablebranchautodeletion): Boolean
  [EnvironmentVariables](#cfn-amplify-app-environmentvariables): 
    - EnvironmentVariable
  [IAMServiceRole](#cfn-amplify-app-iamservicerole): String
  [Name](#cfn-amplify-app-name): String
  [OauthToken](#cfn-amplify-app-oauthtoken): String
  [Repository](#cfn-amplify-app-repository): String
  [Tags](#cfn-amplify-app-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-amplify-app-properties"></a>

`AccessToken`  <a name="cfn-amplify-app-accesstoken"></a>
 Personal Access token for 3rd party source control system for an Amplify App, used to create webhook and read\-only deploy key\. Token is not stored\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutoBranchCreationConfig`  <a name="cfn-amplify-app-autobranchcreationconfig"></a>
 Sets the configuration for your automatic branch creation\.   
*Required*: No  
*Type*: [AutoBranchCreationConfig](aws-properties-amplify-app-autobranchcreationconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BasicAuthConfig`  <a name="cfn-amplify-app-basicauthconfig"></a>
 The credentials for basic authorization for an Amplify app\.   
*Required*: No  
*Type*: [BasicAuthConfig](aws-properties-amplify-app-basicauthconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BuildSpec`  <a name="cfn-amplify-app-buildspec"></a>
 The build specification \(build spec\) for an Amplify app\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomHeaders`  <a name="cfn-amplify-app-customheaders"></a>
The custom HTTP headers for an Amplify app\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomRules`  <a name="cfn-amplify-app-customrules"></a>
 The custom rewrite and redirect rules for an Amplify app\.   
*Required*: No  
*Type*: List of [CustomRule](aws-properties-amplify-app-customrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-amplify-app-description"></a>
 The description for an Amplify app\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableBranchAutoDeletion`  <a name="cfn-amplify-app-enablebranchautodeletion"></a>
Automatically disconnect a branch in the Amplify Console when you delete a branch from your Git repository\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnvironmentVariables`  <a name="cfn-amplify-app-environmentvariables"></a>
 The environment variables map for an Amplify app\.   
*Required*: No  
*Type*: List of [EnvironmentVariable](aws-properties-amplify-app-environmentvariable.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IAMServiceRole`  <a name="cfn-amplify-app-iamservicerole"></a>
 The AWS Identity and Access Management \(IAM\) service role for the Amazon Resource Name \(ARN\) of the Amplify app\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-amplify-app-name"></a>
 The name for an Amplify app\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OauthToken`  <a name="cfn-amplify-app-oauthtoken"></a>
 The OAuth token for a third\-party source control system for an Amplify app\. The OAuth token is used to create a webhook and a read\-only deploy key\. The OAuth token is not stored\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Repository`  <a name="cfn-amplify-app-repository"></a>
 The repository for an Amplify app\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-amplify-app-tags"></a>
 The tag for an Amplify app\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-amplify-app-return-values"></a>

### Fn::GetAtt<a name="aws-resource-amplify-app-return-values-fn--getatt"></a>

#### <a name="aws-resource-amplify-app-return-values-fn--getatt-fn--getatt"></a>

`AppId`  <a name="AppId-fn::getatt"></a>
Unique Id for the Amplify App\.

`AppName`  <a name="AppName-fn::getatt"></a>
Name for the Amplify App\.

`Arn`  <a name="Arn-fn::getatt"></a>
ARN for the Amplify App\.

`DefaultDomain`  <a name="DefaultDomain-fn::getatt"></a>
Default domain for the Amplify App\.