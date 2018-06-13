# AWS::CodePipeline::CustomActionType<a name="aws-resource-codepipeline-customactiontype"></a>

The `AWS::CodePipeline::CustomActionType` resource creates a custom action for activities that aren't included in the AWS CodePipeline default actions, such as running an internally developed build process or a test suite\. You can use these custom actions in the stage of a [pipeline](aws-resource-codepipeline-pipeline.md)\. For more information, see [Create and Add a Custom Action in AWS CodePipeline](http://docs.aws.amazon.com/codepipeline/latest/userguide/how-to-create-custom-action.html) in the *AWS CodePipeline User Guide*\.

**Topics**
+ [Syntax](#aws-resource-codepipeline-customactiontype-syntax)
+ [Properties](#w3ab2c21c10d263b9)
+ [Return Value](#w3ab2c21c10d263c11)
+ [Example](#w3ab2c21c10d263c13)

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
    "[Version](#cfn-codepipeline-customactiontype-version)" : String
  }
}
```

### YAML<a name="aws-resource-codepipeline-customactiontype-syntax.yaml"></a>

```
Type: "AWS::CodePipeline::CustomActionType"
Properties:
  [Category](#cfn-codepipeline-customactiontype-category): String,
  [ConfigurationProperties](#cfn-codepipeline-customactiontype-configurationproperties):
    - ConfigurationProperties
  [InputArtifactDetails](#cfn-codepipeline-customactiontype-inputartifactdetails):
    ArtifactDetails
  [OutputArtifactDetails](#cfn-codepipeline-customactiontype-outputartifactdetails):
    ArtifactDetails
  [Provider](#cfn-codepipeline-customactiontype-provider): String
  [Settings](#cfn-codepipeline-customactiontype-settings):
    Settings
  [Version](#cfn-codepipeline-customactiontype-version): String
```

## Properties<a name="w3ab2c21c10d263b9"></a>

`Category`  <a name="cfn-codepipeline-customactiontype-category"></a>
The category of the custom action, such as a source action or a build action\. For valid values, see [CreateCustomActionType](http://docs.aws.amazon.com/codepipeline/latest/APIReference/API_CreateCustomActionType.html) in the *AWS CodePipeline API Reference*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ConfigurationProperties`  <a name="cfn-codepipeline-customactiontype-configurationproperties"></a>
The configuration properties for the custom action\.  
*Required*: No  
*Type*: List of [AWS CodePipeline CustomActionType ConfigurationProperties](aws-resource-codepipeline-customactiontype-configurationproperties.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`InputArtifactDetails`  <a name="cfn-codepipeline-customactiontype-inputartifactdetails"></a>
The input artifact details for this custom action\.  
*Required*: Yes  
*Type*: [AWS CodePipeline CustomActionType ArtifactDetails](aws-resource-codepipeline-customactiontype-artifactdetails.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`OutputArtifactDetails`  <a name="cfn-codepipeline-customactiontype-outputartifactdetails"></a>
The output artifact details for this custom action\.  
*Required*: Yes  
*Type*: [AWS CodePipeline CustomActionType ArtifactDetails](aws-resource-codepipeline-customactiontype-artifactdetails.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Provider`  <a name="cfn-codepipeline-customactiontype-provider"></a>
The name of the service provider that AWS CodePipeline uses for this custom action\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Settings`  <a name="cfn-codepipeline-customactiontype-settings"></a>
URLs that provide users information about this custom action\.  
*Required*: No  
*Type*: [AWS CodePipeline CustomActionType Settings](aws-resource-codepipeline-customactiontype-settings.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Version`  <a name="cfn-codepipeline-customactiontype-version"></a>
The version number of this custom action\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Value<a name="w3ab2c21c10d263c11"></a>

### Ref<a name="w3ab2c21c10d263c11b2"></a>

When you pass the logical ID of an `AWS::CodePipeline::CustomActionType` resource to the intrinsic `Ref` function, the function returns the custom action name, such as `custo-MyCus-A1BCDEFGHIJ2`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d263c13"></a>

The following example is a custom build action that requires users to specify one property: a project name\.

### JSON<a name="aws-resource-codepipeline-customactiontype-example.json"></a>

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
    }
  }
}
```

### YAML<a name="aws-resource-codepipeline-customactiontype-example.yaml"></a>

```
MyCustomActionType: 
  Type: "AWS::CodePipeline::CustomActionType"
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
```