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
      "[AutoBranchCreationConfig](#cfn-amplify-app-autobranchcreationconfig)" : [AutoBranchCreationConfig](aws-properties-amplify-app-autobranchcreationconfig.md),
      "[BasicAuthConfig](#cfn-amplify-app-basicauthconfig)" : [BasicAuthConfig](aws-properties-amplify-app-basicauthconfig.md),
      "[BuildSpec](#cfn-amplify-app-buildspec)" : String,
      "[CustomRules](#cfn-amplify-app-customrules)" : [ [CustomRule](aws-properties-amplify-app-customrule.md), ... ],
      "[Description](#cfn-amplify-app-description)" : String,
      "[EnvironmentVariables](#cfn-amplify-app-environmentvariables)" : [ [EnvironmentVariable](aws-properties-amplify-app-environmentvariable.md), ... ],
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
    [AutoBranchCreationConfig](aws-properties-amplify-app-autobranchcreationconfig.md)
  [BasicAuthConfig](#cfn-amplify-app-basicauthconfig): 
    [BasicAuthConfig](aws-properties-amplify-app-basicauthconfig.md)
  [BuildSpec](#cfn-amplify-app-buildspec): String
  [CustomRules](#cfn-amplify-app-customrules): 
    - [CustomRule](aws-properties-amplify-app-customrule.md)
  [Description](#cfn-amplify-app-description): String
  [EnvironmentVariables](#cfn-amplify-app-environmentvariables): 
    - [EnvironmentVariable](aws-properties-amplify-app-environmentvariable.md)
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
 Credentials for Basic Authorization for an Amplify App\.   
*Required*: No  
*Type*: [BasicAuthConfig](aws-properties-amplify-app-basicauthconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BuildSpec`  <a name="cfn-amplify-app-buildspec"></a>
 BuildSpec for an Amplify App   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomRules`  <a name="cfn-amplify-app-customrules"></a>
 Custom rewrite / redirect rules for an Amplify App\.   
*Required*: No  
*Type*: List of [CustomRule](aws-properties-amplify-app-customrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-amplify-app-description"></a>
 Description for an Amplify App   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnvironmentVariables`  <a name="cfn-amplify-app-environmentvariables"></a>
 Environment variables map for an Amplify App\.   
*Required*: No  
*Type*: List of [EnvironmentVariable](aws-properties-amplify-app-environmentvariable.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IAMServiceRole`  <a name="cfn-amplify-app-iamservicerole"></a>
 IAM service role ARN for the Amplify App\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-amplify-app-name"></a>
 Name for the Amplify App   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OauthToken`  <a name="cfn-amplify-app-oauthtoken"></a>
 OAuth token for 3rd party source control system for an Amplify App, used to create webhook and read\-only deploy key\. OAuth token is not stored\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Repository`  <a name="cfn-amplify-app-repository"></a>
 Repository for an Amplify App   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-amplify-app-tags"></a>
 Tag for an Amplify App   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-amplify-app-return-values"></a>

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

## Supported Regions

This ResourceType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-west-2`
