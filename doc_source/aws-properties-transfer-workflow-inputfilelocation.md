# AWS::Transfer::Workflow InputFileLocation<a name="aws-properties-transfer-workflow-inputfilelocation"></a>

<a name="aws-properties-transfer-workflow-inputfilelocation-description"></a>The `InputFileLocation` property type specifies Property description not available\. for an [AWS::Transfer::Workflow](aws-resource-transfer-workflow.md)\.

## Syntax<a name="aws-properties-transfer-workflow-inputfilelocation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-transfer-workflow-inputfilelocation-syntax.json"></a>

```
{
  "[EfsFileLocation](#cfn-transfer-workflow-inputfilelocation-efsfilelocation)" : EfsInputFileLocation,
  "[S3FileLocation](#cfn-transfer-workflow-inputfilelocation-s3filelocation)" : S3InputFileLocation
}
```

### YAML<a name="aws-properties-transfer-workflow-inputfilelocation-syntax.yaml"></a>

```
  [EfsFileLocation](#cfn-transfer-workflow-inputfilelocation-efsfilelocation): 
    EfsInputFileLocation
  [S3FileLocation](#cfn-transfer-workflow-inputfilelocation-s3filelocation): 
    S3InputFileLocation
```

## Properties<a name="aws-properties-transfer-workflow-inputfilelocation-properties"></a>

`EfsFileLocation`  <a name="cfn-transfer-workflow-inputfilelocation-efsfilelocation"></a>
Property description not available\.  
*Required*: No  
*Type*: [EfsInputFileLocation](aws-properties-transfer-workflow-efsinputfilelocation.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`S3FileLocation`  <a name="cfn-transfer-workflow-inputfilelocation-s3filelocation"></a>
Property description not available\.  
*Required*: No  
*Type*: [S3InputFileLocation](aws-properties-transfer-workflow-s3inputfilelocation.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)