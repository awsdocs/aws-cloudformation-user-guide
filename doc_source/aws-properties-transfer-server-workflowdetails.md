# AWS::Transfer::Server WorkflowDetails<a name="aws-properties-transfer-server-workflowdetails"></a>

Container for the `WorkflowDetail` data type\. It is used by actions that trigger a workflow to begin execution\.

## Syntax<a name="aws-properties-transfer-server-workflowdetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-transfer-server-workflowdetails-syntax.json"></a>

```
{
  "[OnPartialUpload](#cfn-transfer-server-workflowdetails-onpartialupload)" : [ WorkflowDetail, ... ],
  "[OnUpload](#cfn-transfer-server-workflowdetails-onupload)" : [ WorkflowDetail, ... ]
}
```

### YAML<a name="aws-properties-transfer-server-workflowdetails-syntax.yaml"></a>

```
  [OnPartialUpload](#cfn-transfer-server-workflowdetails-onpartialupload): 
    - WorkflowDetail
  [OnUpload](#cfn-transfer-server-workflowdetails-onupload): 
    - WorkflowDetail
```

## Properties<a name="aws-properties-transfer-server-workflowdetails-properties"></a>

`OnPartialUpload`  <a name="cfn-transfer-server-workflowdetails-onpartialupload"></a>
A trigger that starts a workflow if a file is only partially uploaded\. You can attach a workflow to a server that executes whenever there is a partial upload\.  
A *partial upload* occurs when a file is open when the session disconnects\.  
*Required*: No  
*Type*: List of [WorkflowDetail](aws-properties-transfer-server-workflowdetail.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OnUpload`  <a name="cfn-transfer-server-workflowdetails-onupload"></a>
A trigger that starts a workflow: the workflow begins to execute after a file is uploaded\.  
To remove an associated workflow from a server, you can provide an empty `OnUpload` object, as in the following example\.  
 `aws transfer update-server --server-id s-01234567890abcdef --workflow-details '{"OnUpload":[]}'`   
*Required*: No  
*Type*: List of [WorkflowDetail](aws-properties-transfer-server-workflowdetail.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)