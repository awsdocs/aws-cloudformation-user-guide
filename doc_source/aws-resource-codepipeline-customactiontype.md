# AWS::CodePipeline::CustomActionType<a name="aws-resource-codepipeline-customactiontype"></a>

The `AWS::CodePipeline::CustomActionType` resource creates a custom action for activities that aren't included in the CodePipeline default actions, such as running an internally developed build process or a test suite\. You can use these custom actions in the stage of a pipeline\. For more information, see [Create and Add a Custom Action in AWS CodePipeline](https://docs.aws.amazon.com/codepipeline/latest/userguide/how-to-create-custom-action.html) in the *AWS CodePipeline User Guide*\. 

## Syntax<a name="aws-resource-codepipeline-customactiontype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-codepipeline-customactiontype-syntax.json"></a>

```
{
  "Type" : "AWS::CodePipeline::CustomActionType",
  "Properties" : {
      "[Category](#cfn-codepipeline-customactiontype-category)" : String,
      "[ConfigurationProperties](#cfn-codepipeline-customactiontype-configurationproperties)" : [ ConfigurationProperties, ... ],
      "[InputArtifactDetails](#cfn-codepipeline-customactiontype-inputartifactdetails)" : ArtifactDetails,
      "[OutputArtifactDetails](#cfn-codepipeline-customactiontype-outputartifactdetails)" : ArtifactDetails,
      "[Provider](#cfn-codepipeline-customactiontype-provider)" : String,
      "[Settings](#cfn-codepipeline-customactiontype-settings)" : Settings,
      "[Tags](#cfn-codepipeline-customactiontype-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Version](#cfn-codepipeline-customactiontype-version)" : String
    }
}
```

### YAML<a name="aws-resource-codepipeline-customactiontype-syntax.yaml"></a>

```
Type: AWS::CodePipeline::CustomActionType
Properties: 
  [Category](#cfn-codepipeline-customactiontype-category): String
  [ConfigurationProperties](#cfn-codepipeline-customactiontype-configurationproperties): 
    - ConfigurationProperties
  [InputArtifactDetails](#cfn-codepipeline-customactiontype-inputartifactdetails): 
    ArtifactDetails
  [OutputArtifactDetails](#cfn-codepipeline-customactiontype-outputartifactdetails): 
    ArtifactDetails
  [Provider](#cfn-codepipeline-customactiontype-provider): String
  [Settings](#cfn-codepipeline-customactiontype-settings): 
    Settings
  [Tags](#cfn-codepipeline-customactiontype-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Version](#cfn-codepipeline-customactiontype-version): String
```

## Properties<a name="aws-resource-codepipeline-customactiontype-properties"></a>

`Category`  <a name="cfn-codepipeline-customactiontype-category"></a>
The category of the custom action, such as a build action or a test action\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Approval | Build | Deploy | Invoke | Source | Test`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConfigurationProperties`  <a name="cfn-codepipeline-customactiontype-configurationproperties"></a>
The configuration properties for the custom action\.  
You can refer to a name in the configuration properties of the custom action within the URL templates by following the format of \{Config:name\}, as long as the configuration property is both required and not secret\. For more information, see [Create a Custom Action for a Pipeline](https://docs.aws.amazon.com/codepipeline/latest/userguide/how-to-create-custom-action.html)\.
*Required*: No  
*Type*: [List](aws-properties-codepipeline-customactiontype-configurationproperties.md) of [ConfigurationProperties](aws-properties-codepipeline-customactiontype-configurationproperties.md)  
*Maximum*: `10`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InputArtifactDetails`  <a name="cfn-codepipeline-customactiontype-inputartifactdetails"></a>
The details of the input artifact for the action, such as its commit ID\.  
*Required*: Yes  
*Type*: [ArtifactDetails](aws-properties-codepipeline-customactiontype-artifactdetails.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OutputArtifactDetails`  <a name="cfn-codepipeline-customactiontype-outputartifactdetails"></a>
The details of the output artifact of the action, such as its commit ID\.  
*Required*: Yes  
*Type*: [ArtifactDetails](aws-properties-codepipeline-customactiontype-artifactdetails.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Provider`  <a name="cfn-codepipeline-customactiontype-provider"></a>
The provider of the service used in the custom action, such as AWS CodeDeploy\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `25`  
*Pattern*: `[0-9A-Za-z_-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Settings`  <a name="cfn-codepipeline-customactiontype-settings"></a>
URLs that provide users information about this custom action\.  
*Required*: No  
*Type*: [Settings](aws-properties-codepipeline-customactiontype-settings.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-codepipeline-customactiontype-tags"></a>
The tags for the custom action\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-codepipeline-customactiontype-version"></a>
The version identifier of the custom action\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `9`  
*Pattern*: `[0-9A-Za-z_-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-codepipeline-customactiontype-return-values"></a>

### Ref<a name="aws-resource-codepipeline-customactiontype-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the custom action name, such as custo\-MyCus\-A1BCDEFGHIJ2\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-codepipeline-customactiontype--examples"></a>



### Custom Action Type Resource Configuration<a name="aws-resource-codepipeline-customactiontype--examples--Custom_Action_Type_Resource_Configuration"></a>

The following example is a custom build action that requires users to specify one property: a project name\.

#### JSON<a name="aws-resource-codepipeline-customactiontype--examples--Custom_Action_Type_Resource_Configuration--json"></a>

```
"MyCustomActionType": { 
  "Type": "AWS::CodePipeline::CustomActionType", 
  "Properties": { 
    "Category": "Build", 
    "Provider": "My-Build-Provider-Name", 
    "Version": { "Ref" : "Version" }, 
    "ConfigurationProperties": [ 
      {
        "Description": "The name of the build project must be provided when this action is added to the pipeline.", 
        "Key": "true", 
        "Name": "MyProjectName", 
        "Queryable": "false", 
        "Required": "true", 
        "Secret": "false", 
        "Type": "String" 
      } 
    ], 
    "InputArtifactDetails": { 
      "MaximumCount": "1", 
      "MinimumCount": "1" 
    }, 
    "OutputArtifactDetails": { 
      "MaximumCount": { "Ref" : "MaximumCountForOutputArtifactDetails" }, 
      "MinimumCount": "0" 
    }, 
    "Settings": {
      "EntityUrlTemplate": "https://my-build-instance/job/{Config:ProjectName}/",
      "ExecutionUrlTemplate": "https://my-build-instance/job/{Config:ProjectName}/lastSuccessfulBuild/{ExternalExecutionId}/"
    },
    "Tags": [
      {
        "Key": "Project",
        "Value": "ProjectA"
      },
      {
        "Key": "Team",
        "Value": "Admins"
      }
    ]
  } 
}
```

#### YAML<a name="aws-resource-codepipeline-customactiontype--examples--Custom_Action_Type_Resource_Configuration--yaml"></a>

```
MyCustomActionType: 
  Type: AWS::CodePipeline::CustomActionType
  Properties: 
    Category: Build 
    Provider: "My-Build-Provider-Name" 
    Version: 
      Ref: Version
    ConfigurationProperties: 
      - 
        Description: "The name of the build project must be provided when this action is added to the pipeline." 
        Key: true 
        Name: MyProjectName 
        Queryable: false
        Required: true 
        Secret: false 
        Type: String 
    InputArtifactDetails: 
      MaximumCount: 1
      MinimumCount: 1 
    OutputArtifactDetails: 
      MaximumCount: 
        Ref: MaximumCountForOutputArtifactDetails 
      MinimumCount: 0 
    Settings: 
      EntityUrlTemplate: "https://my-build-instance/job/{Config:ProjectName}/" 
      ExecutionUrlTemplate: "https://my-build-instance/job/{Config:ProjectName}/lastSuccessfulBuild/{ExternalExecutionId}/"
    Tags:
      - Key: Project
        Value: ProjectA
      - Key: Team
        Value: Admins
```