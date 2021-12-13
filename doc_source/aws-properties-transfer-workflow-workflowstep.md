# AWS::Transfer::Workflow WorkflowStep<a name="aws-properties-transfer-workflow-workflowstep"></a>

The basic building block of a workflow\.

## Syntax<a name="aws-properties-transfer-workflow-workflowstep-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-transfer-workflow-workflowstep-syntax.json"></a>

```
{
  "[CopyStepDetails](#cfn-transfer-workflow-workflowstep-copystepdetails)" : Json,
  "[CustomStepDetails](#cfn-transfer-workflow-workflowstep-customstepdetails)" : Json,
  "[DeleteStepDetails](#cfn-transfer-workflow-workflowstep-deletestepdetails)" : Json,
  "[TagStepDetails](#cfn-transfer-workflow-workflowstep-tagstepdetails)" : Json,
  "[Type](#cfn-transfer-workflow-workflowstep-type)" : String
}
```

### YAML<a name="aws-properties-transfer-workflow-workflowstep-syntax.yaml"></a>

```
  [CopyStepDetails](#cfn-transfer-workflow-workflowstep-copystepdetails): Json
  [CustomStepDetails](#cfn-transfer-workflow-workflowstep-customstepdetails): Json
  [DeleteStepDetails](#cfn-transfer-workflow-workflowstep-deletestepdetails): Json
  [TagStepDetails](#cfn-transfer-workflow-workflowstep-tagstepdetails): Json
  [Type](#cfn-transfer-workflow-workflowstep-type): String
```

## Properties<a name="aws-properties-transfer-workflow-workflowstep-properties"></a>

`CopyStepDetails`  <a name="cfn-transfer-workflow-workflowstep-copystepdetails"></a>
Details for a step that performs a file copy\. Consists of the following values:  
+ A description
+ An S3 location for the destination of the file copy
+ A flag that indicates whether or not to overwrite an existing file of the same name\. The default is `FALSE`\.
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CustomStepDetails`  <a name="cfn-transfer-workflow-workflowstep-customstepdetails"></a>
Details for a step that invokes a lambda function\. Consists of the lambda function name, target, and timeout \(in seconds\)\.  
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DeleteStepDetails`  <a name="cfn-transfer-workflow-workflowstep-deletestepdetails"></a>
Details for a step that deletes the file\.  
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TagStepDetails`  <a name="cfn-transfer-workflow-workflowstep-tagstepdetails"></a>
Details for a step that creates one or more tags\. You specify one or more tags: each tag contains a key/value pair\.  
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-transfer-workflow-workflowstep-type"></a>
Currently, the following step types are supported\.  
+ *Copy*: copy the file to another location
+ *Custom*: custom step with a lambda target
+ *Delete*: delete the file
+ *Tag*: add a tag to the file
*Required*: No  
*Type*: String  
*Allowed values*: `COPY | CUSTOM | DELETE | TAG`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)