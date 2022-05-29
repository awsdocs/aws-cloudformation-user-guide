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