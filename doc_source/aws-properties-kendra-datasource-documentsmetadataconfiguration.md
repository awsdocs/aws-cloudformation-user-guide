# AWS::Kendra::DataSource DocumentsMetadataConfiguration<a name="aws-properties-kendra-datasource-documentsmetadataconfiguration"></a>

Document metadata files that contain information such as the document access control information, source URI, document author, and custom attributes\. Each metadata file contains metadata about a single document\.

## Syntax<a name="aws-properties-kendra-datasource-documentsmetadataconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-documentsmetadataconfiguration-syntax.json"></a>

```
{
  "[S3Prefix](#cfn-kendra-datasource-documentsmetadataconfiguration-s3prefix)" : String
}
```

### YAML<a name="aws-properties-kendra-datasource-documentsmetadataconfiguration-syntax.yaml"></a>

```
  [S3Prefix](#cfn-kendra-datasource-documentsmetadataconfiguration-s3prefix): String
```

## Properties<a name="aws-properties-kendra-datasource-documentsmetadataconfiguration-properties"></a>

`S3Prefix`  <a name="cfn-kendra-datasource-documentsmetadataconfiguration-s3prefix"></a>
A prefix used to filter metadata configuration files in the AWS S3 bucket\. The S3 bucket might contain multiple metadata files\. Use `S3Prefix` to include only the desired metadata files\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)