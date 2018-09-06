# AWS::CodePipeline::Pipeline<a name="aws-resource-codepipeline-pipeline"></a>

The `AWS::CodePipeline::Pipeline` resource creates an AWS CodePipeline pipeline that describes how software changes go through a release process\. For more information, see [What Is AWS CodePipeline?](http://docs.aws.amazon.com/codepipeline/latest/userguide/welcome.html) in the *AWS CodePipeline User Guide*\.

**Topics**
+ [Syntax](#aws-resource-codepipeline-pipeline-syntax)
+ [Properties](#w3ab2c21c10d267b9)
+ [Return Value](#w3ab2c21c10d267c11)
+ [Example](#w3ab2c21c10d267c13)

## Syntax<a name="aws-resource-codepipeline-pipeline-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-codepipeline-pipeline-syntax.json"></a>

```
{
  "Type" : "AWS::CodePipeline::Pipeline",
  "Properties" : {
    "[ArtifactStore](#cfn-codepipeline-pipeline-artifactstore)" : ArtifactStore,
    "[DisableInboundStageTransitions](#cfn-codepipeline-pipeline-disableinboundstagetransitions)" : [ DisableInboundStageTransitions, ... ],
    "[Name](#cfn-codepipeline-pipeline-name)" : String,
    "[RestartExecutionOnUpdate](#cfn-codepipeline-pipeline-restartexecutiononupdate)" : Boolean,
    "[RoleArn](#cfn-codepipeline-pipeline-rolearn)" : String,
    "[Stages](#cfn-codepipeline-pipeline-stages)" : [ Stages, ... ]
  }
}
```

### YAML<a name="aws-resource-codepipeline-pipeline-syntax.yaml"></a>

```
Type: "AWS::CodePipeline::Pipeline"
Properties:
  [ArtifactStore](#cfn-codepipeline-pipeline-artifactstore):
    ArtifactStore
  [DisableInboundStageTransitions](#cfn-codepipeline-pipeline-disableinboundstagetransitions):
    - DisableInboundStageTransitions
  [Name](#cfn-codepipeline-pipeline-name): String
  [RestartExecutionOnUpdate](#cfn-codepipeline-pipeline-restartexecutiononupdate): Boolean
  [RoleArn](#cfn-codepipeline-pipeline-rolearn): String
  [Stages](#cfn-codepipeline-pipeline-stages):
    - Stages
```

## Properties<a name="w3ab2c21c10d267b9"></a>

`ArtifactStore`  <a name="cfn-codepipeline-pipeline-artifactstore"></a>
The Amazon Simple Storage Service \(Amazon S3\) location where AWS CodePipeline stores pipeline artifacts\. For more information, see [Create an Amazon S3 Bucket for Your Application](http://docs.aws.amazon.com/codepipeline/latest/userguide/getting-started-w.html) in the *AWS CodePipeline User Guide*\.  
*Required*: Yes  
*Type*: [AWS CodePipeline Pipeline ArtifactStore](aws-properties-codepipeline-pipeline-artifactstore.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DisableInboundStageTransitions`  <a name="cfn-codepipeline-pipeline-disableinboundstagetransitions"></a>
Prevents artifacts in a pipeline from transitioning to the stage that you specified\. This enables you to manually control transitions\.  
*Required*: No  
*Type*: List of [AWS CodePipeline Pipeline DisableInboundStageTransitions](aws-properties-codepipeline-pipeline-disableinboundstagetransitions.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Name`  <a name="cfn-codepipeline-pipeline-name"></a>
The name of your AWS CodePipeline pipeline\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RestartExecutionOnUpdate`  <a name="cfn-codepipeline-pipeline-restartexecutiononupdate"></a>
Indicates whether to rerun the AWS CodePipeline pipeline after you update it\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RoleArn`  <a name="cfn-codepipeline-pipeline-rolearn"></a>
A service role Amazon Resource Name \(ARN\) that grants AWS CodePipeline permission to make calls to AWS services on your behalf\. For more information, see [AWS CodePipeline Access Permissions Reference](http://docs.aws.amazon.com/codepipeline/latest/userguide/access-permissions.html) in the *AWS CodePipeline User Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Stages`  <a name="cfn-codepipeline-pipeline-stages"></a>
Defines the AWS CodePipeline pipeline stages\.  
*Required*: Yes  
*Type*: [AWS CodePipeline Pipeline Stages](aws-properties-codepipeline-pipeline-stages.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10d267c11"></a>

### Ref<a name="w3ab2c21c10d267c11b2"></a>

When you pass the logical ID of an `AWS::CodePipeline::Pipeline` resource to the intrinsic `Ref` function, the function returns the pipeline name, such as `mysta-MyPipeline-A1BCDEFGHIJ2`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d267c13"></a>

The following example creates a pipeline with a source, beta, and release stage\. For the source stage, AWS CodePipeline detects changes to the application that is stored in the S3 bucket and pulls them into the pipeline\. The beta stage deploys those changes to EC2 instances by using AWS CodeDeploy\. For the release stage, inbound transitions are disabled, which enables you to control when the changes are ready to be deployed to release\.

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
  Type: "AWS::CodePipeline::Pipeline"
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