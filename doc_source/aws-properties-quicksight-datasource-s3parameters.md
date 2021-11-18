# AWS::QuickSight::DataSource S3Parameters<a name="aws-properties-quicksight-datasource-s3parameters"></a>

The parameters for S3\.

## Syntax<a name="aws-properties-quicksight-datasource-s3parameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-datasource-s3parameters-syntax.json"></a>

```
{
  "[ManifestFileLocation](#cfn-quicksight-datasource-s3parameters-manifestfilelocation)" : ManifestFileLocation
}
```

### YAML<a name="aws-properties-quicksight-datasource-s3parameters-syntax.yaml"></a>

```
  [ManifestFileLocation](#cfn-quicksight-datasource-s3parameters-manifestfilelocation): 
    ManifestFileLocation
```

## Properties<a name="aws-properties-quicksight-datasource-s3parameters-properties"></a>

`ManifestFileLocation`  <a name="cfn-quicksight-datasource-s3parameters-manifestfilelocation"></a>
Location of the Amazon S3 manifest file\. This is NULL if the manifest file was uploaded into Amazon QuickSight\.  
*Required*: Yes  
*Type*: [ManifestFileLocation](aws-properties-quicksight-datasource-manifestfilelocation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)