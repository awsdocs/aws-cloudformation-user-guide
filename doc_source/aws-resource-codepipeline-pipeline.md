# AWS::CodePipeline::Pipeline<a name="aws-resource-codepipeline-pipeline"></a>

The `AWS::CodePipeline::Pipeline` resource creates a CodePipeline pipeline that describes how software changes go through a release process\. For more information, see [What Is CodePipeline?](https://docs.aws.amazon.com/codepipeline/latest/userguide/welcome.html) in the *AWS CodePipeline User Guide*\. 

## Syntax<a name="aws-resource-codepipeline-pipeline-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-codepipeline-pipeline-syntax.json"></a>

```
{
  "Type" : "AWS::CodePipeline::Pipeline",
  "Properties" : {
      "[ArtifactStore](#cfn-codepipeline-pipeline-artifactstore)" : ArtifactStore,
      "[ArtifactStores](#cfn-codepipeline-pipeline-artifactstores)" : [ ArtifactStoreMap, ... ],
      "[DisableInboundStageTransitions](#cfn-codepipeline-pipeline-disableinboundstagetransitions)" : [ StageTransition, ... ],
      "[Name](#cfn-codepipeline-pipeline-name)" : String,
      "[RestartExecutionOnUpdate](#cfn-codepipeline-pipeline-restartexecutiononupdate)" : Boolean,
      "[RoleArn](#cfn-codepipeline-pipeline-rolearn)" : String,
      "[Stages](#cfn-codepipeline-pipeline-stages)" : [ StageDeclaration, ... ],
      "[Tags](#cfn-codepipeline-pipeline-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-codepipeline-pipeline-syntax.yaml"></a>

```
Type: AWS::CodePipeline::Pipeline
Properties: 
  [ArtifactStore](#cfn-codepipeline-pipeline-artifactstore): 
    ArtifactStore
  [ArtifactStores](#cfn-codepipeline-pipeline-artifactstores): 
    - ArtifactStoreMap
  [DisableInboundStageTransitions](#cfn-codepipeline-pipeline-disableinboundstagetransitions): 
    - StageTransition
  [Name](#cfn-codepipeline-pipeline-name): String
  [RestartExecutionOnUpdate](#cfn-codepipeline-pipeline-restartexecutiononupdate): Boolean
  [RoleArn](#cfn-codepipeline-pipeline-rolearn): String
  [Stages](#cfn-codepipeline-pipeline-stages): 
    - StageDeclaration
  [Tags](#cfn-codepipeline-pipeline-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-codepipeline-pipeline-properties"></a>

`ArtifactStore`  <a name="cfn-codepipeline-pipeline-artifactstore"></a>
The S3 bucket where artifacts for the pipeline are stored\.  
You must include either `artifactStore` or `artifactStores` in your pipeline, but you cannot use both\. If you create a cross\-region action in your pipeline, you must use `artifactStores`\.
*Required*: Conditional  
*Type*: [ArtifactStore](aws-properties-codepipeline-pipeline-artifactstore.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ArtifactStores`  <a name="cfn-codepipeline-pipeline-artifactstores"></a>
A mapping of `artifactStore` objects and their corresponding AWS Regions\. There must be an artifact store for the pipeline Region and for each cross\-region action in the pipeline\.  
You must include either `artifactStore` or `artifactStores` in your pipeline, but you cannot use both\. If you create a cross\-region action in your pipeline, you must use `artifactStores`\.
*Required*: Conditional  
*Type*: List of [ArtifactStoreMap](aws-properties-codepipeline-pipeline-artifactstoremap.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisableInboundStageTransitions`  <a name="cfn-codepipeline-pipeline-disableinboundstagetransitions"></a>
Represents the input of a `DisableStageTransition` action\.  
*Required*: No  
*Type*: List of [StageTransition](aws-properties-codepipeline-pipeline-disableinboundstagetransitions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-codepipeline-pipeline-name"></a>
The name of the pipeline\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `[A-Za-z0-9.@\-_]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RestartExecutionOnUpdate`  <a name="cfn-codepipeline-pipeline-restartexecutiononupdate"></a>
Indicates whether to rerun the CodePipeline pipeline after you update it\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-codepipeline-pipeline-rolearn"></a>
The Amazon Resource Name \(ARN\) for AWS CodePipeline to use to either perform actions with no `actionRoleArn`, or to use to assume roles for actions with an `actionRoleArn`\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `arn:aws(-[\w]+)*:iam::[0-9]{12}:role/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Stages`  <a name="cfn-codepipeline-pipeline-stages"></a>
Represents information about a stage and its definition\.  
*Required*: Yes  
*Type*: List of [StageDeclaration](aws-properties-codepipeline-pipeline-stages.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-codepipeline-pipeline-tags"></a>
Specifies the tags applied to the pipeline\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-codepipeline-pipeline-return-values"></a>

### Ref<a name="aws-resource-codepipeline-pipeline-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the pipeline name, such as mysta\-MyPipeline\-A1BCDEFGHIJ2\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-codepipeline-pipeline-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-codepipeline-pipeline-return-values-fn--getatt-fn--getatt"></a>

`Version`  <a name="Version-fn::getatt"></a>
The version of the pipeline\.  
A new pipeline is always assigned a version number of 1\. This number increments when a pipeline is updated\.

## Examples<a name="aws-resource-codepipeline-pipeline--examples"></a>



### Pipeline Resource Configuration<a name="aws-resource-codepipeline-pipeline--examples--Pipeline_Resource_Configuration"></a>

The following example creates a pipeline with a source, beta, and release stage\. For the source stage, CodePipeline detects changes to the application that is stored in the S3 bucket and pulls them into the pipeline\. The beta stage deploys those changes to EC2 instances by using CodeDeploy\. For the release stage, inbound transitions are disabled, which enables you to control when the changes are ready to be deployed to release\.

#### JSON<a name="aws-resource-codepipeline-pipeline--examples--Pipeline_Resource_Configuration--json"></a>

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
              { "Name": "SourceOutput" 
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
      "Location": { "Ref" : "ArtifactStoreS3Location" },
      "EncryptionKey": {
        "Id": "arn:aws:kms:useast-1:ACCOUNT-ID:key/KEY-ID",
        "Type": "KMS"
      }, 
    "DisableInboundStageTransitions": [ 
      {
        "StageName": "Release", 
        "Reason": "Disabling the transition until integration tests are completed" 
      } 
    ],
    "Tags": [
      {
        "Key": "Project",
        "Value": "ProjectA"
      },
      {
        "Key": "IsContainerBased",
        "Value": "true"
      }
    ]
  } 
}
```

#### YAML<a name="aws-resource-codepipeline-pipeline--examples--Pipeline_Resource_Configuration--yaml"></a>

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
      EncryptionKey:
        Id: arn:aws:kms:useast-1:ACCOUNT-ID:key/KEY-ID
        Type: KMS
    DisableInboundStageTransitions: 
      - 
        StageName: Release 
        Reason: "Disabling the transition until integration tests are completed"
    Tags:
      - Key: Project
        Value: ProjectA
      - Key: IsContainerBased
        Value: 'true'
```