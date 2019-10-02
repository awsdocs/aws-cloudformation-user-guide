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
      "[BasicAuthConfig](#cfn-amplify-branch-basicauthconfig)" : [BasicAuthConfig](aws-properties-amplify-branch-basicauthconfig.md),
      "[BranchName](#cfn-amplify-branch-branchname)" : String,
      "[BuildSpec](#cfn-amplify-branch-buildspec)" : String,
      "[Description](#cfn-amplify-branch-description)" : String,
      "[EnableAutoBuild](#cfn-amplify-branch-enableautobuild)" : Boolean,
      "[EnvironmentVariables](#cfn-amplify-branch-environmentvariables)" : [ [EnvironmentVariable](aws-properties-amplify-branch-environmentvariable.md), ... ],
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
    [BasicAuthConfig](aws-properties-amplify-branch-basicauthconfig.md)
  [BranchName](#cfn-amplify-branch-branchname): String
  [BuildSpec](#cfn-amplify-branch-buildspec): String
  [Description](#cfn-amplify-branch-description): String
  [EnableAutoBuild](#cfn-amplify-branch-enableautobuild): Boolean
  [EnvironmentVariables](#cfn-amplify-branch-environmentvariables): 
    - [EnvironmentVariable](aws-properties-amplify-branch-environmentvariable.md)
  [Stage](#cfn-amplify-branch-stage): String
  [Tags](#cfn-amplify-branch-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-amplify-branch-properties"></a>

`AppId`  <a name="cfn-amplify-branch-appid"></a>
 Unique Id for an Amplify App\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BasicAuthConfig`  <a name="cfn-amplify-branch-basicauthconfig"></a>
 Basic Authorization credentials for a branch, part of an Amplify App\.   
*Required*: No  
*Type*: [BasicAuthConfig](aws-properties-amplify-branch-basicauthconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BranchName`  <a name="cfn-amplify-branch-branchname"></a>
 Name for the branch\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BuildSpec`  <a name="cfn-amplify-branch-buildspec"></a>
 BuildSpec for the branch\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-amplify-branch-description"></a>
 Description for the branch\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableAutoBuild`  <a name="cfn-amplify-branch-enableautobuild"></a>
 Enables auto building for the branch\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnvironmentVariables`  <a name="cfn-amplify-branch-environmentvariables"></a>
 Environment Variables for the branch\.   
*Required*: No  
*Type*: List of [EnvironmentVariable](aws-properties-amplify-branch-environmentvariable.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Stage`  <a name="cfn-amplify-branch-stage"></a>
 Stage for the branch\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-amplify-branch-tags"></a>
 Tag for the branch\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-amplify-branch-return-values"></a>

### Fn::GetAtt<a name="aws-resource-amplify-branch-return-values-fn--getatt"></a>

#### <a name="aws-resource-amplify-branch-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
 ARN for a branch, part of an Amplify App\. 

`BranchName`  <a name="BranchName-fn::getatt"></a>
 Name for a branch, part of an Amplify App\. 

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
