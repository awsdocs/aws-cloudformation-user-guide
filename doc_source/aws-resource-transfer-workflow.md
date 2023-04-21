# AWS::Transfer::Workflow<a name="aws-resource-transfer-workflow"></a>

 Allows you to create a workflow with specified steps and step details the workflow invokes after file transfer completes\. After creating a workflow, you can associate the workflow created with any transfer servers by specifying the `workflow-details` field in `CreateServer` and `UpdateServer` operations\. 

## Syntax<a name="aws-resource-transfer-workflow-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-transfer-workflow-syntax.json"></a>

```
{
  "Type" : "AWS::Transfer::Workflow",
  "Properties" : {
      "[Description](#cfn-transfer-workflow-description)" : String,
      "[OnExceptionSteps](#cfn-transfer-workflow-onexceptionsteps)" : [ WorkflowStep, ... ],
      "[Steps](#cfn-transfer-workflow-steps)" : [ WorkflowStep, ... ],
      "[Tags](#cfn-transfer-workflow-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-transfer-workflow-syntax.yaml"></a>

```
Type: AWS::Transfer::Workflow
Properties: 
  [Description](#cfn-transfer-workflow-description): String
  [OnExceptionSteps](#cfn-transfer-workflow-onexceptionsteps): 
    - WorkflowStep
  [Steps](#cfn-transfer-workflow-steps): 
    - WorkflowStep
  [Tags](#cfn-transfer-workflow-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-transfer-workflow-properties"></a>

`Description`  <a name="cfn-transfer-workflow-description"></a>
Specifies the text description for the workflow\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `^[\w- ]*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OnExceptionSteps`  <a name="cfn-transfer-workflow-onexceptionsteps"></a>
Specifies the steps \(actions\) to take if errors are encountered during execution of the workflow\.  
*Required*: No  
*Type*: List of [WorkflowStep](aws-properties-transfer-workflow-workflowstep.md)  
*Maximum*: `8`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Steps`  <a name="cfn-transfer-workflow-steps"></a>
Specifies the details for the steps that are in the specified workflow\.  
*Required*: Yes  
*Type*: List of [WorkflowStep](aws-properties-transfer-workflow-workflowstep.md)  
*Maximum*: `8`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-transfer-workflow-tags"></a>
Key\-value pairs that can be used to group and search for workflows\. Tags are metadata attached to workflows for any purpose\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-transfer-workflow-return-values"></a>

### Ref<a name="aws-resource-transfer-workflow-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-transfer-workflow-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-transfer-workflow-return-values-fn--getatt-fn--getatt"></a>

`WorkflowId`  <a name="WorkflowId-fn::getatt"></a>
A unique identifier for a workflow\.

## Examples<a name="aws-resource-transfer-workflow--examples"></a>

### Create workflow from a file<a name="aws-resource-transfer-workflow--examples--Create_workflow_from_a_file"></a>

You can save workflow step information into a text file, and then use that file to create a workflow, as in the following example\. The following example assumes you have saved your workflow steps into ` example-file.json ` \(in the same folder from where you run the command\), and that you wish to create the workflow in the N\. Virginia \(us\-east\-1\) region\. 

#### <a name="aws-resource-transfer-workflow--examples--Create_workflow_from_a_file--shell"></a>

```
aws transfer create-workflow --description "example workflow from a file" --steps file://example-file.json --region us-east-1
```

### Create workflow from a template<a name="aws-resource-transfer-workflow--examples--Create_workflow_from_a_template"></a>

You can create a workflow from a template\. First, open the CloudFormation console\. Next, follow the instructions for deploying AWS CloudFormation stack from an existing template in [Selecting a stack template](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-using-console-create-stack-template.html) in the *AWS CloudFormation User Guide*\.

Save the following code to a file, and upload it to CloudFormation when prompted, making sure to replace items as follows:
+ Replace `your-workflow-execution-role-arn` with the ARN for an actual workflow execution role\.
+ replace `arn:${AWS::Partition}:lambda:${AWS::Region}:${AWS::AccountId}:function:my-function-name` with the ARN for your Lambda function\. For example, `arn:aws:lambda:us-east-2:123456789012:function:example-lambda-idp`\.

#### JSON<a name="aws-resource-transfer-workflow--examples--Create_workflow_from_a_template--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "SFTPServer": {
            "Type": "AWS::Transfer::Server",
            "Properties": {
                "WorkflowDetails": {
                    "OnUpload": [
                        {
                            "ExecutionRole": "your-workflow-execution-role-arn",
                            "WorkflowId": {
                                "Fn::GetAtt": [
                                    "TransferWorkflow",
                                    "WorkflowId"
                                ]
                            }
                        }
                    ]
                }
            }
        },
        "TransferWorkflow": {
            "Type": "AWS::Transfer::Workflow",
            "Properties": {
                "Description": "Transfer Family Workflows Blog",
                "Steps": [
                    {
                        "Type": "COPY",
                        "CopyStepDetails": {
                            "Name": "copyToUserKey",
                            "DestinationFileLocation": {
                                "S3FileLocation": {
                                    "Bucket": "archived-records",
                                    "Key": "${transfer:UserName}/"
                                }
                            },
                            "OverwriteExisting": "TRUE"
                        }
                    },
                    {
                        "Type": "TAG",
                        "TagStepDetails": {
                            "Name": "tagFileForArchive",
                            "Tags": [
                                {
                                    "Key": "Archive",
                                    "Value": "yes"
                                }
                            ]
                        }
                    },
                    {
                        "Type": "CUSTOM",
                        "CustomStepDetails": {
                            "Name": "transferExtract",
                            "Target": "arn:${AWS::Partition}:lambda:${AWS::Region}:${AWS::AccountId}:function:my-function-name",
                            "TimeoutSeconds": 60
                        }
                    },
                    {
                        "Type": "DELETE",
                        "DeleteStepDetails": {
                            "Name": "DeleteInputFile",
                            "SourceFileLocation": "${original.file}"
                        }
                    }
                ],
                "Tags": [
                    {
                        "Key": "Name",
                        "Value": "TransferFamilyWorkflows"
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-transfer-workflow--examples--Create_workflow_from_a_template--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  SFTPServer:
    Type: 'AWS::Transfer::Server'
    Properties:
      WorkflowDetails:
        OnUpload:
          - ExecutionRole: your-workflow-execution-role-arn
            WorkflowId: !GetAtt
              - TransferWorkflow
              - WorkflowId
  TransferWorkflow:
    Type: AWS::Transfer::Workflow
    Properties:
      Description: Transfer Family Workflows Blog
      Steps:
        - Type: COPY
          CopyStepDetails:
            Name: copyToUserKey
            DestinationFileLocation:
              S3FileLocation:
                Bucket: archived-records
                Key: ${transfer:UserName}/
            OverwriteExisting: 'TRUE'
        - Type: TAG
          TagStepDetails:
            Name: tagFileForArchive
            Tags:
              - Key: Archive
                Value: yes
        - Type: CUSTOM
          CustomStepDetails:
            Name: transferExtract
            Target: arn:${AWS::Partition}:lambda:${AWS::Region}:${AWS::AccountId}:function:my-function-name
            TimeoutSeconds: 60
        - Type: DELETE
          DeleteStepDetails:
            Name: DeleteInputFile
            SourceFileLocation: '${original.file}'
      Tags:
        - Key: Name
          Value: TransferFamilyWorkflows
```