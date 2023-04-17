# AWS::Transfer::Workflow S3InputFileLocation<a name="aws-properties-transfer-workflow-s3inputfilelocation"></a>

Specifies the details for the Amazon S3 location for an input file to a workflow\.

## Syntax<a name="aws-properties-transfer-workflow-s3inputfilelocation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-transfer-workflow-s3inputfilelocation-syntax.json"></a>

```
{
  "[Bucket](#cfn-transfer-workflow-s3inputfilelocation-bucket)" : String,
  "[Key](#cfn-transfer-workflow-s3inputfilelocation-key)" : String
}
```

### YAML<a name="aws-properties-transfer-workflow-s3inputfilelocation-syntax.yaml"></a>

```
  [Bucket](#cfn-transfer-workflow-s3inputfilelocation-bucket): String
  [Key](#cfn-transfer-workflow-s3inputfilelocation-key): String
```

## Properties<a name="aws-properties-transfer-workflow-s3inputfilelocation-properties"></a>

`Bucket`  <a name="cfn-transfer-workflow-s3inputfilelocation-bucket"></a>
Specifies the S3 bucket for the customer input file\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Key`  <a name="cfn-transfer-workflow-s3inputfilelocation-key"></a>
The name assigned to the file when it was created in Amazon S3\. You use the object key to retrieve the object\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)