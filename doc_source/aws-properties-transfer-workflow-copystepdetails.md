# AWS::Transfer::Workflow CopyStepDetails<a name="aws-properties-transfer-workflow-copystepdetails"></a>

Details for a step that performs a file copy\.

 Consists of the following values: 
+ A description
+ An Amazon S3 location for the destination of the file copy\.
+ A flag that indicates whether to overwrite an existing file of the same name\. The default is `FALSE`\.

## Syntax<a name="aws-properties-transfer-workflow-copystepdetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-transfer-workflow-copystepdetails-syntax.json"></a>

```
{
  "[DestinationFileLocation](#cfn-transfer-workflow-copystepdetails-destinationfilelocation)" : S3FileLocation,
  "[Name](#cfn-transfer-workflow-copystepdetails-name)" : String,
  "[OverwriteExisting](#cfn-transfer-workflow-copystepdetails-overwriteexisting)" : String,
  "[SourceFileLocation](#cfn-transfer-workflow-copystepdetails-sourcefilelocation)" : String
}
```

### YAML<a name="aws-properties-transfer-workflow-copystepdetails-syntax.yaml"></a>

```
  [DestinationFileLocation](#cfn-transfer-workflow-copystepdetails-destinationfilelocation): 
    S3FileLocation
  [Name](#cfn-transfer-workflow-copystepdetails-name): String
  [OverwriteExisting](#cfn-transfer-workflow-copystepdetails-overwriteexisting): String
  [SourceFileLocation](#cfn-transfer-workflow-copystepdetails-sourcefilelocation): String
```

## Properties<a name="aws-properties-transfer-workflow-copystepdetails-properties"></a>

`DestinationFileLocation`  <a name="cfn-transfer-workflow-copystepdetails-destinationfilelocation"></a>
Specifies the location for the file being copied\. Use `${Transfer:UserName}` or `${Transfer:UploadDate}` in this field to parametrize the destination prefix by username or uploaded date\.  
+ Set the value of `DestinationFileLocation` to `${Transfer:UserName}` to copy uploaded files to an Amazon S3 bucket that is prefixed with the name of the Transfer Family user that uploaded the file\.
+ Set the value of `DestinationFileLocation` to `${Transfer:UploadDate}` to copy uploaded files to an Amazon S3 bucket that is prefixed with the date of the upload\.
**Note**  
The system resolves `UploadDate` to a date format of *YYYY\-MM\-DD*, based on the date the file is uploaded in UTC\.
*Required*: No  
*Type*: [S3FileLocation](aws-properties-transfer-workflow-s3filelocation.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-transfer-workflow-copystepdetails-name"></a>
The name of the step, used as an identifier\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OverwriteExisting`  <a name="cfn-transfer-workflow-copystepdetails-overwriteexisting"></a>
A flag that indicates whether to overwrite an existing file of the same name\. The default is `FALSE`\.  
If the workflow is processing a file that has the same name as an existing file, the behavior is as follows:  
+ If `OverwriteExisting` is `TRUE`, the existing file is replaced with the file being processed\.
+ If `OverwriteExisting` is `FALSE`, nothing happens, and the workflow processing stops\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceFileLocation`  <a name="cfn-transfer-workflow-copystepdetails-sourcefilelocation"></a>
Specifies which file to use as input to the workflow step: either the output from the previous step, or the originally uploaded file for the workflow\.  
+ To use the previous file as the input, enter `${previous.file}`\. In this case, this workflow step uses the output file from the previous workflow step as input\. This is the default value\.
+ To use the originally uploaded file location as input for this step, enter `${original.file}`\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)