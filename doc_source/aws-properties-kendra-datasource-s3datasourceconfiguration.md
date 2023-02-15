# AWS::Kendra::DataSource S3DataSourceConfiguration<a name="aws-properties-kendra-datasource-s3datasourceconfiguration"></a>

Provides the configuration information to connect to an Amazon S3 bucket\.

## Syntax<a name="aws-properties-kendra-datasource-s3datasourceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-s3datasourceconfiguration-syntax.json"></a>

```
{
  "[AccessControlListConfiguration](#cfn-kendra-datasource-s3datasourceconfiguration-accesscontrollistconfiguration)" : AccessControlListConfiguration,
  "[BucketName](#cfn-kendra-datasource-s3datasourceconfiguration-bucketname)" : String,
  "[DocumentsMetadataConfiguration](#cfn-kendra-datasource-s3datasourceconfiguration-documentsmetadataconfiguration)" : DocumentsMetadataConfiguration,
  "[ExclusionPatterns](#cfn-kendra-datasource-s3datasourceconfiguration-exclusionpatterns)" : [ String, ... ],
  "[InclusionPatterns](#cfn-kendra-datasource-s3datasourceconfiguration-inclusionpatterns)" : [ String, ... ],
  "[InclusionPrefixes](#cfn-kendra-datasource-s3datasourceconfiguration-inclusionprefixes)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-kendra-datasource-s3datasourceconfiguration-syntax.yaml"></a>

```
  [AccessControlListConfiguration](#cfn-kendra-datasource-s3datasourceconfiguration-accesscontrollistconfiguration): 
    AccessControlListConfiguration
  [BucketName](#cfn-kendra-datasource-s3datasourceconfiguration-bucketname): String
  [DocumentsMetadataConfiguration](#cfn-kendra-datasource-s3datasourceconfiguration-documentsmetadataconfiguration): 
    DocumentsMetadataConfiguration
  [ExclusionPatterns](#cfn-kendra-datasource-s3datasourceconfiguration-exclusionpatterns): 
    - String
  [InclusionPatterns](#cfn-kendra-datasource-s3datasourceconfiguration-inclusionpatterns): 
    - String
  [InclusionPrefixes](#cfn-kendra-datasource-s3datasourceconfiguration-inclusionprefixes): 
    - String
```

## Properties<a name="aws-properties-kendra-datasource-s3datasourceconfiguration-properties"></a>

`AccessControlListConfiguration`  <a name="cfn-kendra-datasource-s3datasourceconfiguration-accesscontrollistconfiguration"></a>
Provides the path to the S3 bucket that contains the user context filtering files for the data source\. For the format of the file, see [Access control for S3 data sources](https://docs.aws.amazon.com/kendra/latest/dg/s3-acl.html)\.  
*Required*: No  
*Type*: [AccessControlListConfiguration](aws-properties-kendra-datasource-accesscontrollistconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BucketName`  <a name="cfn-kendra-datasource-s3datasourceconfiguration-bucketname"></a>
The name of the bucket that contains the documents\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Pattern*: `[a-z0-9][\.\-a-z0-9]{1,61}[a-z0-9]`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentsMetadataConfiguration`  <a name="cfn-kendra-datasource-s3datasourceconfiguration-documentsmetadataconfiguration"></a>
Specifies document metadata files that contain information such as the document access control information, source URI, document author, and custom attributes\. Each metadata file contains metadata about a single document\.  
*Required*: No  
*Type*: [DocumentsMetadataConfiguration](aws-properties-kendra-datasource-documentsmetadataconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExclusionPatterns`  <a name="cfn-kendra-datasource-s3datasourceconfiguration-exclusionpatterns"></a>
A list of glob patterns for documents that should not be indexed\. If a document that matches an inclusion prefix or inclusion pattern also matches an exclusion pattern, the document is not indexed\.  
Some [examples](https://docs.aws.amazon.com/cli/latest/reference/s3/#use-of-exclude-and-include-filters) are:  
+  *\*\.png , \*\.jpg* will exclude all PNG and JPEG image files in a directory \(files with the extensions \.png and \.jpg\)\.
+  *\*internal\** will exclude all files in a directory that contain 'internal' in the file name, such as 'internal', 'internal\_only', 'company\_internal'\.
+  *\*\*/\*internal\** will exclude all internal\-related files in a directory and its subdirectories\.
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InclusionPatterns`  <a name="cfn-kendra-datasource-s3datasourceconfiguration-inclusionpatterns"></a>
A list of glob patterns for documents that should be indexed\. If a document that matches an inclusion pattern also matches an exclusion pattern, the document is not indexed\.  
Some [examples](https://docs.aws.amazon.com/cli/latest/reference/s3/#use-of-exclude-and-include-filters) are:  
+  *\*\.txt* will include all text files in a directory \(files with the extension \.txt\)\.
+  *\*\*/\*\.txt* will include all text files in a directory and its subdirectories\.
+  *\*tax\** will include all files in a directory that contain 'tax' in the file name, such as 'tax', 'taxes', 'income\_tax'\.
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InclusionPrefixes`  <a name="cfn-kendra-datasource-s3datasourceconfiguration-inclusionprefixes"></a>
A list of S3 prefixes for the documents that should be included in the index\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)