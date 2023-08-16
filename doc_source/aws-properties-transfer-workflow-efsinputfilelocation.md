# AWS::Transfer::Workflow EfsInputFileLocation<a name="aws-properties-transfer-workflow-efsinputfilelocation"></a>

Specifies the Amazon EFS identifier and the path for the file being used\.

## Syntax<a name="aws-properties-transfer-workflow-efsinputfilelocation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-transfer-workflow-efsinputfilelocation-syntax.json"></a>

```
{
  "[FileSystemId](#cfn-transfer-workflow-efsinputfilelocation-filesystemid)" : String,
  "[Path](#cfn-transfer-workflow-efsinputfilelocation-path)" : String
}
```

### YAML<a name="aws-properties-transfer-workflow-efsinputfilelocation-syntax.yaml"></a>

```
  [FileSystemId](#cfn-transfer-workflow-efsinputfilelocation-filesystemid): String
  [Path](#cfn-transfer-workflow-efsinputfilelocation-path): String
```

## Properties<a name="aws-properties-transfer-workflow-efsinputfilelocation-properties"></a>

`FileSystemId`  <a name="cfn-transfer-workflow-efsinputfilelocation-filesystemid"></a>
The identifier of the file system, assigned by Amazon EFS\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Path`  <a name="cfn-transfer-workflow-efsinputfilelocation-path"></a>
The pathname for the folder being used by a workflow\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)