# AWS::CodePipeline::Pipeline<a name="aws-resource-codepipeline-pipeline"></a>

The `AWS::CodePipeline::Pipeline` resource creates an CodePipeline pipeline that describes how software changes go through a release process\. For more information, see [What Is CodePipeline?](https://docs.aws.amazon.com/codepipeline/latest/userguide/welcome.html) in the *AWS CodePipeline User Guide*\.

## Syntax<a name="aws-resource-codepipeline-pipeline-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-codepipeline-pipeline-syntax.json"></a>

```
{
  "Type" : "AWS::CodePipeline::Pipeline",
  "Properties" : {
    "[ArtifactStore](#cfn-codepipeline-pipeline-artifactstore)" : [ArtifactStore](aws-properties-codepipeline-pipeline-artifactstore.md),
    "[ArtifactStores](#cfn-codepipeline-pipeline-artifactstores)" : [ [ArtifactStoreMap](aws-properties-codepipeline-pipeline-artifactstoremap.md), ... ],
    "[DisableInboundStageTransitions](#cfn-codepipeline-pipeline-disableinboundstagetransitions)" : [ [DisableInboundStageTransitions](aws-properties-codepipeline-pipeline-disableinboundstagetransitions.md), ... ],
    "[Name](#cfn-codepipeline-pipeline-name)" : String,
    "[RestartExecutionOnUpdate](#cfn-codepipeline-pipeline-restartexecutiononupdate)" : Boolean,
    "[RoleArn](#cfn-codepipeline-pipeline-rolearn)" : String,
    "[Stages](#cfn-codepipeline-pipeline-stages)" : [ [Stages](aws-properties-codepipeline-pipeline-stages.md), ... ]
  }
}
```

### YAML<a name="aws-resource-codepipeline-pipeline-syntax.yaml"></a>

```
Type: AWS::CodePipeline::Pipeline
Properties:
  [ArtifactStore](#cfn-codepipeline-pipeline-artifactstore):
    [ArtifactStore](aws-properties-codepipeline-pipeline-artifactstore.md)
  [ArtifactStores](#cfn-codepipeline-pipeline-artifactstores):
    - [ArtifactStoreMap](aws-properties-codepipeline-pipeline-artifactstoremap.md)
  [DisableInboundStageTransitions](#cfn-codepipeline-pipeline-disableinboundstagetransitions):
    - [DisableInboundStageTransitions](aws-properties-codepipeline-pipeline-disableinboundstagetransitions.md)
  [Name](#cfn-codepipeline-pipeline-name): String
  [RestartExecutionOnUpdate](#cfn-codepipeline-pipeline-restartexecutiononupdate): Boolean
  [RoleArn](#cfn-codepipeline-pipeline-rolearn): String
  [Stages](#cfn-codepipeline-pipeline-stages):
    - [Stages](aws-properties-codepipeline-pipeline-stages.md)
```

## Properties<a name="w13ab1c21c10c81c17b9"></a>

`ArtifactStore`  <a name="cfn-codepipeline-pipeline-artifactstore"></a>
The Amazon Simple Storage Service \(Amazon S3\) location where CodePipeline stores pipeline artifacts\. You can only use either `ArtifactStore` or `ArtifactStores`, not both\. For more information, see [Create an Amazon S3 Bucket for Your Application](https://docs.aws.amazon.com/codepipeline/latest/userguide/getting-started-w.html) in the *AWS CodePipeline User Guide*\.  
*Required*: No  
*Type*: [ArtifactStore](aws-properties-codepipeline-pipeline-artifactstore.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ArtifactStores`  <a name="cfn-codepipeline-pipeline-artifactstores"></a>
Specifies a list of `ArtifactStoreMap` mappings\. There must be an artifact store for the pipeline region and for each cross\-region action within the pipeline\. You can only use either `ArtifactStore` or `ArtifactStores`, not both\.  
*Required*: No  
*Type*: List of [ArtifactStoreMap](aws-properties-codepipeline-pipeline-artifactstoremap.md) property types  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DisableInboundStageTransitions`  <a name="cfn-codepipeline-pipeline-disableinboundstagetransitions"></a>
Prevents artifacts in a pipeline from transitioning to the stage that you specified\. This enables you to manually control transitions\.  
*Required*: No  
*Type*: List of [DisableInboundStageTransitions](aws-properties-codepipeline-pipeline-disableinboundstagetransitions.md) property types  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Name`  <a name="cfn-codepipeline-pipeline-name"></a>
The name of your CodePipeline pipeline\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RestartExecutionOnUpdate`  <a name="cfn-codepipeline-pipeline-restartexecutiononupdate"></a>
Indicates whether to rerun the CodePipeline pipeline after you update it\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RoleArn`  <a name="cfn-codepipeline-pipeline-rolearn"></a>
A service role Amazon Resource Name \(ARN\) that grants AWS CodePipeline permission to make calls to AWS services on your behalf\. For more information, see [AWS CodePipeline Access Permissions Reference](https://docs.aws.amazon.com/codepipeline/latest/userguide/access-permissions.html) in the *AWS CodePipeline User Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Stages`  <a name="cfn-codepipeline-pipeline-stages"></a>
Defines the CodePipeline pipeline stages\.  
*Required*: Yes  
*Type*: List of [Stages](aws-properties-codepipeline-pipeline-stages.md) property types  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w13ab1c21c10c81c17c11"></a>

### Ref<a name="w13ab1c21c10c81c17c11b2"></a>

When you pass the logical ID of an `AWS::CodePipeline::Pipeline` resource to the intrinsic `Ref` function, the function returns the pipeline name, such as `mysta-MyPipeline-A1BCDEFGHIJ2`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-resource-codepipeline-pipeline-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`Version`  
The version of the pipeline\.  
A new pipeline is always assigned a version number of 1\. This number increments when a pipeline is updated\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Example<a name="w13ab1c21c10c81c17c13"></a>

The following example creates a pipeline with a source, beta, and release stage\. For the source stage, CodePipeline detects changes to the application that is stored in the S3 bucket and pulls them into the pipeline\. The beta stage deploys those changes to EC2 instances by using CodeDeploy\. For the release stage, inbound transitions are disabled, which enables you to control when the changes are ready to be deployed to release\.

### JSON<a name="aws-resource-codepipeline-pipeline-example.json"></a>

```
"AppPipeline": {
  "Type": "AWS::CodePipeline::Pipeline",
  "Properties": {
    "RoleArn": { "Ref" : "CodePipelineServiceRole" },
    "Stages": [
      {
        "Name": "Source",
        "Actions": [
          {
            "Name": "SourceAction",
            "ActionTypeId": {
              "Category": "Source",
              "Owner": "AWS",
              "Version": "1",
              "Provider": "S3"
            },
            "OutputArtifacts": [
              {
                "Name": "SourceOutput"
              }
            ],
            "Configuration": {
              "S3Bucket": { "Ref" : "SourceS3Bucket" },
              "S3ObjectKey": { "Ref" : "SourceS3ObjectKey" }
            },
            "RunOrder": 1
          }
        ]
      },
      {
        "Name": "Beta",
        "Actions": [
          {
            "Name": "BetaAction",
            "InputArtifacts": [
              {
                "Name": "SourceOutput"
              }
            ],
            "ActionTypeId": {
              "Category": "Deploy",
              "Owner": "AWS",
              "Version": "1",
              "Provider": "CodeDeploy"
            },
            "Configuration": {
              "ApplicationName": {"Ref" : "ApplicationName"},
              "DeploymentGroupName": {"Ref" : "DeploymentGroupName"}
            },
            "RunOrder": 1
          }
        ]
      },
      {
        "Name": "Release",
        "Actions": [
          {
            "Name": "ReleaseAction",
            "InputArtifacts": [
              {
                "Name": "SourceOutput"
              }
            ],
            "ActionTypeId": {
              "Category": "Deploy",
              "Owner": "AWS",
              "Version": "1",
              "Provider": "CodeDeploy"
            },
            "Configuration": {
              "ApplicationName": {"Ref" : "ApplicationName"},
              "DeploymentGroupName": {"Ref" : "DeploymentGroupName"}
            },
            "RunOrder": 1
          }
        ]
      }
    ],
    "ArtifactStore": {
      "Type": "S3",
      "Location": { "Ref" : "ArtifactStoreS3Location" }
    },
    "DisableInboundStageTransitions": [
      {
        "StageName": "Release",
        "Reason": "Disabling the transition until integration tests are completed"
      }
    ]
  }
}
```

### YAML<a name="aws-resource-codepipeline-pipeline-example.yaml"></a>

```
AppPipeline: 
  Type: AWS::CodePipeline::Pipeline
  Properties: 
    RoleArn: 
      Ref: CodePipelineServiceRole
    Stages: 
      - 
        Name: Source
        Actions: 
          - 
            Name: SourceAction
            ActionTypeId: 
              Category: Source
              Owner: AWS
              Version: 1
              Provider: S3
            OutputArtifacts: 
              - 
                Name: SourceOutput
            Configuration: 
              S3Bucket: 
                Ref: SourceS3Bucket
              S3ObjectKey: 
                Ref: SourceS3ObjectKey
            RunOrder: 1
      - 
        Name: Beta
        Actions: 
          - 
            Name: BetaAction
            InputArtifacts: 
              - 
                Name: SourceOutput
            ActionTypeId: 
              Category: Deploy
              Owner: AWS
              Version: 1
              Provider: CodeDeploy
            Configuration: 
              ApplicationName: 
                Ref: ApplicationName
              DeploymentGroupName: 
                Ref: DeploymentGroupName
            RunOrder: 1
      - 
        Name: Release
        Actions: 
          - 
            Name: ReleaseAction
            InputArtifacts: 
              - 
                Name: SourceOutput
            ActionTypeId: 
              Category: Deploy
              Owner: AWS
              Version: 1
              Provider: CodeDeploy
            Configuration: 
              ApplicationName: 
                Ref: ApplicationName
              DeploymentGroupName: 
                Ref: DeploymentGroupName
            RunOrder: 1
    ArtifactStore: 
      Type: S3
      Location: 
        Ref: ArtifactStoreS3Location
    DisableInboundStageTransitions: 
      - 
        StageName: Release
        Reason: "Disabling the transition until integration tests are completed"
```