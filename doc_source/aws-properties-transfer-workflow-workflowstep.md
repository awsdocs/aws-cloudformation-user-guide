# AWS::Transfer::Workflow WorkflowStep<a name="aws-properties-transfer-workflow-workflowstep"></a>

The basic building block of a workflow\.

## Syntax<a name="aws-properties-transfer-workflow-workflowstep-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-transfer-workflow-workflowstep-syntax.json"></a>

```
{
  "[CopyStepDetails](#cfn-transfer-workflow-workflowstep-copystepdetails)" : CopyStepDetails,
  "[CustomStepDetails](#cfn-transfer-workflow-workflowstep-customstepdetails)" : CustomStepDetails,
  "[DecryptStepDetails](#cfn-transfer-workflow-workflowstep-decryptstepdetails)" : DecryptStepDetails,
  "[DeleteStepDetails](#cfn-transfer-workflow-workflowstep-deletestepdetails)" : DeleteStepDetails,
  "[TagStepDetails](#cfn-transfer-workflow-workflowstep-tagstepdetails)" : TagStepDetails,
  "[Type](#cfn-transfer-workflow-workflowstep-type)" : String
}
```

### YAML<a name="aws-properties-transfer-workflow-workflowstep-syntax.yaml"></a>

```
  [CopyStepDetails](#cfn-transfer-workflow-workflowstep-copystepdetails): 
    CopyStepDetails
  [CustomStepDetails](#cfn-transfer-workflow-workflowstep-customstepdetails): 
    CustomStepDetails
  [DecryptStepDetails](#cfn-transfer-workflow-workflowstep-decryptstepdetails): 
    DecryptStepDetails
  [DeleteStepDetails](#cfn-transfer-workflow-workflowstep-deletestepdetails): 
    DeleteStepDetails
  [TagStepDetails](#cfn-transfer-workflow-workflowstep-tagstepdetails): 
    TagStepDetails
  [Type](#cfn-transfer-workflow-workflowstep-type): String
```

## Properties<a name="aws-properties-transfer-workflow-workflowstep-properties"></a>

`CopyStepDetails`  <a name="cfn-transfer-workflow-workflowstep-copystepdetails"></a>
Details for a step that performs a file copy\.  
 Consists of the following values:   
+ A description
+ An Amazon S3 location for the destination of the file copy\.
+ A flag that indicates whether to overwrite an existing file of the same name\. The default is `FALSE`\.
*Required*: No  
*Type*: [CopyStepDetails](aws-properties-transfer-workflow-copystepdetails.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CustomStepDetails`  <a name="cfn-transfer-workflow-workflowstep-customstepdetails"></a>
Details for a step that invokes an AWS Lambda function\.  
Consists of the Lambda function's name, target, and timeout \(in seconds\)\.   
*Required*: No  
*Type*: [CustomStepDetails](aws-properties-transfer-workflow-customstepdetails.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DecryptStepDetails`  <a name="cfn-transfer-workflow-workflowstep-decryptstepdetails"></a>
Property description not available\.  
*Required*: No  
*Type*: [DecryptStepDetails](aws-properties-transfer-workflow-decryptstepdetails.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DeleteStepDetails`  <a name="cfn-transfer-workflow-workflowstep-deletestepdetails"></a>
Details for a step that deletes the file\.  
*Required*: No  
*Type*: [DeleteStepDetails](aws-properties-transfer-workflow-deletestepdetails.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TagStepDetails`  <a name="cfn-transfer-workflow-workflowstep-tagstepdetails"></a>
Details for a step that creates one or more tags\.  
You specify one or more tags\. Each tag contains a key\-value pair\.  
*Required*: No  
*Type*: [TagStepDetails](aws-properties-transfer-workflow-tagstepdetails.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-transfer-workflow-workflowstep-type"></a>
 Currently, the following step types are supported\.   
+  ** `COPY` ** \- Copy the file to another location\.
+  ** `CUSTOM` ** \- Perform a custom step with an AWS Lambda function target\.
+  ** `DECRYPT` ** \- Decrypt a file that was encrypted before it was uploaded\.
+  ** `DELETE` ** \- Delete the file\.
+  ** `TAG` ** \- Add a tag to the file\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)