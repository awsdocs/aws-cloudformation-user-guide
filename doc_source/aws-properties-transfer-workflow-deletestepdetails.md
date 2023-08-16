# AWS::Transfer::Workflow DeleteStepDetails<a name="aws-properties-transfer-workflow-deletestepdetails"></a>

An object that contains the name and file location for a file being deleted by a workflow\.

## Syntax<a name="aws-properties-transfer-workflow-deletestepdetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-transfer-workflow-deletestepdetails-syntax.json"></a>

```
{
  "[Name](#cfn-transfer-workflow-deletestepdetails-name)" : String,
  "[SourceFileLocation](#cfn-transfer-workflow-deletestepdetails-sourcefilelocation)" : String
}
```

### YAML<a name="aws-properties-transfer-workflow-deletestepdetails-syntax.yaml"></a>

```
  [Name](#cfn-transfer-workflow-deletestepdetails-name): String
  [SourceFileLocation](#cfn-transfer-workflow-deletestepdetails-sourcefilelocation): String
```

## Properties<a name="aws-properties-transfer-workflow-deletestepdetails-properties"></a>

`Name`  <a name="cfn-transfer-workflow-deletestepdetails-name"></a>
The name of the step, used as an identifier\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceFileLocation`  <a name="cfn-transfer-workflow-deletestepdetails-sourcefilelocation"></a>
Specifies which file to use as input to the workflow step: either the output from the previous step, or the originally uploaded file for the workflow\.  
+ To use the previous file as the input, enter `${previous.file}`\. In this case, this workflow step uses the output file from the previous workflow step as input\. This is the default value\.
+ To use the originally uploaded file location as input for this step, enter `${original.file}`\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)