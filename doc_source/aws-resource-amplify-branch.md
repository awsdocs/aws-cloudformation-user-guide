# AWS::Amplify::Branch<a name="aws-resource-amplify-branch"></a>

 The AWS::Amplify::Branch resource creates a new branch within an app\. 

## Syntax<a name="aws-resource-amplify-branch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-amplify-branch-syntax.json"></a>

```
{
  "Type" : "AWS::Amplify::Branch",
  "Properties" : {
      "[AppId](#cfn-amplify-branch-appid)" : String,
      "[BasicAuthConfig](#cfn-amplify-branch-basicauthconfig)" : BasicAuthConfig,
      "[BranchName](#cfn-amplify-branch-branchname)" : String,
      "[BuildSpec](#cfn-amplify-branch-buildspec)" : String,
      "[Description](#cfn-amplify-branch-description)" : String,
      "[EnableAutoBuild](#cfn-amplify-branch-enableautobuild)" : Boolean,
      "[EnablePerformanceMode](#cfn-amplify-branch-enableperformancemode)" : Boolean,
      "[EnablePullRequestPreview](#cfn-amplify-branch-enablepullrequestpreview)" : Boolean,
      "[EnvironmentVariables](#cfn-amplify-branch-environmentvariables)" : [ EnvironmentVariable, ... ],
      "[PullRequestEnvironmentName](#cfn-amplify-branch-pullrequestenvironmentname)" : String,
      "[Stage](#cfn-amplify-branch-stage)" : String,
      "[Tags](#cfn-amplify-branch-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-amplify-branch-syntax.yaml"></a>

```
Type: AWS::Amplify::Branch
Properties: 
  [AppId](#cfn-amplify-branch-appid): String
  [BasicAuthConfig](#cfn-amplify-branch-basicauthconfig): 
    BasicAuthConfig
  [BranchName](#cfn-amplify-branch-branchname): String
  [BuildSpec](#cfn-amplify-branch-buildspec): String
  [Description](#cfn-amplify-branch-description): String
  [EnableAutoBuild](#cfn-amplify-branch-enableautobuild): Boolean
  [EnablePerformanceMode](#cfn-amplify-branch-enableperformancemode): Boolean
  [EnablePullRequestPreview](#cfn-amplify-branch-enablepullrequestpreview): Boolean
  [EnvironmentVariables](#cfn-amplify-branch-environmentvariables): 
    - EnvironmentVariable
  [PullRequestEnvironmentName](#cfn-amplify-branch-pullrequestenvironmentname): String
  [Stage](#cfn-amplify-branch-stage): String
  [Tags](#cfn-amplify-branch-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-amplify-branch-properties"></a>

`AppId`  <a name="cfn-amplify-branch-appid"></a>
 The unique ID for an Amplify app\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BasicAuthConfig`  <a name="cfn-amplify-branch-basicauthconfig"></a>
 The basic authorization credentials for a branch of an Amplify app\.   
*Required*: No  
*Type*: [BasicAuthConfig](aws-properties-amplify-branch-basicauthconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BranchName`  <a name="cfn-amplify-branch-branchname"></a>
 The name for the branch\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BuildSpec`  <a name="cfn-amplify-branch-buildspec"></a>
 The build specification \(build spec\) for the branch\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-amplify-branch-description"></a>
 The description for the branch\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableAutoBuild`  <a name="cfn-amplify-branch-enableautobuild"></a>
 Enables auto building for the branch\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnablePerformanceMode`  <a name="cfn-amplify-branch-enableperformancemode"></a>
Enables performance mode for the branch\.  
Performance mode optimizes for faster hosting performance by keeping content cached at the edge for a longer interval\. When performance mode is enabled, hosting configuration or code changes can take up to 10 minutes to roll out\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnablePullRequestPreview`  <a name="cfn-amplify-branch-enablepullrequestpreview"></a>
Sets whether the Amplify Console creates a preview for each pull request that is made for this branch\. If this property is enabled, the Amplify Console deploys your app to a unique preview URL after each pull request is opened\. Development and QA teams can use this preview to test the pull request before it's merged into a production or integration branch\.  
To provide backend support for your preview, the Amplify Console automatically provisions a temporary backend environment that it deletes when the pull request is closed\. If you want to specify a dedicated backend environment for your previews, use the `PullRequestEnvironmentName` property\.  
For more information, see [Web Previews](https://docs.aws.amazon.com/amplify/latest/userguide/pr-previews.html) in the *AWS Amplify Console User Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnvironmentVariables`  <a name="cfn-amplify-branch-environmentvariables"></a>
 The environment variables for the branch\.   
*Required*: No  
*Type*: List of [EnvironmentVariable](aws-properties-amplify-branch-environmentvariable.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PullRequestEnvironmentName`  <a name="cfn-amplify-branch-pullrequestenvironmentname"></a>
If pull request previews are enabled for this branch, you can use this property to specify a dedicated backend environment for your previews\. For example, you could specify an environment named `prod`, `test`, or `dev` that you initialized with the Amplify CLI and mapped to this branch\.  
To enable pull request previews, set the `EnablePullRequestPreview` property to `true`\.  
If you don't specify an environment, the Amplify Console provides backend support for each preview by automatically provisioning a temporary backend environment\. Amplify Console deletes this environment when the pull request is closed\.  
For more information about creating backend environments, see [Feature Branch Deployments and Team Workflows](https://docs.aws.amazon.com/amplify/latest/userguide/multi-environments.html) in the *AWS Amplify Console User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Stage`  <a name="cfn-amplify-branch-stage"></a>
 Describes the current stage for the branch\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-amplify-branch-tags"></a>
 The tag for the branch\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-amplify-branch-return-values"></a>

### Fn::GetAtt<a name="aws-resource-amplify-branch-return-values-fn--getatt"></a>

#### <a name="aws-resource-amplify-branch-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
 ARN for a branch, part of an Amplify App\. 

`BranchName`  <a name="BranchName-fn::getatt"></a>
 Name for a branch, part of an Amplify App\. 