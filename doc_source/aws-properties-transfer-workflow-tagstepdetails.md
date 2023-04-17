# AWS::Transfer::Workflow TagStepDetails<a name="aws-properties-transfer-workflow-tagstepdetails"></a>

Details for a step that creates one or more tags\.

You specify one or more tags\. Each tag contains a key\-value pair\.

## Syntax<a name="aws-properties-transfer-workflow-tagstepdetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-transfer-workflow-tagstepdetails-syntax.json"></a>

```
{
  "[Name](#cfn-transfer-workflow-tagstepdetails-name)" : String,
  "[SourceFileLocation](#cfn-transfer-workflow-tagstepdetails-sourcefilelocation)" : String,
  "[Tags](#cfn-transfer-workflow-tagstepdetails-tags)" : [ S3Tag, ... ]
}
```

### YAML<a name="aws-properties-transfer-workflow-tagstepdetails-syntax.yaml"></a>

```
  [Name](#cfn-transfer-workflow-tagstepdetails-name): String
  [SourceFileLocation](#cfn-transfer-workflow-tagstepdetails-sourcefilelocation): String
  [Tags](#cfn-transfer-workflow-tagstepdetails-tags): 
    - S3Tag
```

## Properties<a name="aws-properties-transfer-workflow-tagstepdetails-properties"></a>

`Name`  <a name="cfn-transfer-workflow-tagstepdetails-name"></a>
The name of the step, used as an identifier\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceFileLocation`  <a name="cfn-transfer-workflow-tagstepdetails-sourcefilelocation"></a>
Specifies which file to use as input to the workflow step: either the output from the previous step, or the originally uploaded file for the workflow\.  
+ To use the previous file as the input, enter `${previous.file}`\. In this case, this workflow step uses the output file from the previous workflow step as input\. This is the default value\.
+ To use the originally uploaded file location as input for this step, enter `${original.file}`\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-transfer-workflow-tagstepdetails-tags"></a>
Array that contains from 1 to 10 key/value pairs\.  
*Required*: No  
*Type*: List of [S3Tag](aws-properties-transfer-workflow-s3tag.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)