# AWS::Amplify::App<a name="aws-resource-amplify-app"></a>

 The AWS::Amplify::App resource specifies Apps in Amplify Hosting\. An App is a collection of branches\. 

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
      "[Platform](#cfn-amplify-app-platform)" : String,
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
  [Platform](#cfn-amplify-app-platform): String
  [Repository](#cfn-amplify-app-repository): String
  [Tags](#cfn-amplify-app-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-amplify-app-properties"></a>

`AccessToken`  <a name="cfn-amplify-app-accesstoken"></a>
The personal access token for a GitHub repository for an Amplify app\. The personal access token is used to authorize access to a GitHub repository using the Amplify GitHub App\. The token is not stored\.  
Use `AccessToken` for GitHub repositories only\. To authorize access to a repository provider such as Bitbucket or CodeCommit, use `OauthToken`\.  
You must specify either `AccessToken` or `OauthToken` when you create a new app\.  
Existing Amplify apps deployed from a GitHub repository using OAuth continue to work with CI/CD\. However, we strongly recommend that you migrate these apps to use the GitHub App\. For more information, see [Migrating an existing OAuth app to the Amplify GitHub App](https://docs.aws.amazon.com/amplify/latest/userguide/setting-up-GitHub-access.html#migrating-to-github-app-auth) in the *Amplify User Guide* \.  
*Length Constraints:* Minimum length of 1\. Maximum length of 255\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutoBranchCreationConfig`  <a name="cfn-amplify-app-autobranchcreationconfig"></a>
 Sets the configuration for your automatic branch creation\.   
*Required*: No  
*Type*: [AutoBranchCreationConfig](aws-properties-amplify-app-autobranchcreationconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BasicAuthConfig`  <a name="cfn-amplify-app-basicauthconfig"></a>
 The credentials for basic authorization for an Amplify app\. You must base64\-encode the authorization credentials and provide them in the format `user:password`\.  
*Required*: No  
*Type*: [BasicAuthConfig](aws-properties-amplify-app-basicauthconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BuildSpec`  <a name="cfn-amplify-app-buildspec"></a>
 The build specification \(build spec\) for an Amplify app\.   
*Length Constraints:* Minimum length of 1\. Maximum length of 25000\.  
*Pattern:* \(?s\)\.\+  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomHeaders`  <a name="cfn-amplify-app-customheaders"></a>
The custom HTTP headers for an Amplify app\.  
*Length Constraints:* Minimum length of 0\. Maximum length of 25000\.  
*Pattern:* \(?s\)\.\*  
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
*Length Constraints:* Maximum length of 1000\.  
*Pattern:* \(?s\)\.\*  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableBranchAutoDeletion`  <a name="cfn-amplify-app-enablebranchautodeletion"></a>
Automatically disconnect a branch in Amplify Hosting when you delete a branch from your Git repository\.  
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
*Length Constraints:* Minimum length of 0\. Maximum length of 1000\.  
*Pattern:* \(?s\)\.\*  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-amplify-app-name"></a>
 The name for an Amplify app\.   
*Length Constraints:* Minimum length of 1\. Maximum length of 255\.  
*Pattern:* \(?s\)\.\+  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OauthToken`  <a name="cfn-amplify-app-oauthtoken"></a>
The OAuth token for a third\-party source control system for an Amplify app\. The OAuth token is used to create a webhook and a read\-only deploy key using SSH cloning\. The OAuth token is not stored\.  
Use `OauthToken` for repository providers other than GitHub, such as Bitbucket or CodeCommit\. To authorize access to GitHub as your repository provider, use `AccessToken`\.  
You must specify either `OauthToken` or `AccessToken` when you create a new app\.  
Existing Amplify apps deployed from a GitHub repository using OAuth continue to work with CI/CD\. However, we strongly recommend that you migrate these apps to use the GitHub App\. For more information, see [Migrating an existing OAuth app to the Amplify GitHub App](https://docs.aws.amazon.com/amplify/latest/userguide/setting-up-GitHub-access.html#migrating-to-github-app-auth) in the *Amplify User Guide* \.  
*Length Constraints:* Maximum length of 1000\.  
*Pattern:* \(?s\)\.\*  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Platform`  <a name="cfn-amplify-app-platform"></a>
 The platform for the Amplify app\. For a static app, set the platform type to `WEB`\. For a dynamic server\-side rendered \(SSR\) app, set the platform type to `WEB_COMPUTE`\. For an app requiring Amplify Hosting's original SSR support only, set the platform type to `WEB_DYNAMIC`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Repository`  <a name="cfn-amplify-app-repository"></a>
 The repository for an Amplify app\.   
*Pattern:* \(?s\)\.\*  
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