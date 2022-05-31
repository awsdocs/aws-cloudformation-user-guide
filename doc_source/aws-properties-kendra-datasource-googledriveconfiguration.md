# AWS::Kendra::DataSource GoogleDriveConfiguration<a name="aws-properties-kendra-datasource-googledriveconfiguration"></a>

Provides the configuration information to connect to Google Drive as your data source\.

## Syntax<a name="aws-properties-kendra-datasource-googledriveconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-googledriveconfiguration-syntax.json"></a>

```
{
  "[ExcludeMimeTypes](#cfn-kendra-datasource-googledriveconfiguration-excludemimetypes)" : [ String, ... ],
  "[ExcludeSharedDrives](#cfn-kendra-datasource-googledriveconfiguration-excludeshareddrives)" : [ String, ... ],
  "[ExcludeUserAccounts](#cfn-kendra-datasource-googledriveconfiguration-excludeuseraccounts)" : [ String, ... ],
  "[ExclusionPatterns](#cfn-kendra-datasource-googledriveconfiguration-exclusionpatterns)" : [ String, ... ],
  "[FieldMappings](#cfn-kendra-datasource-googledriveconfiguration-fieldmappings)" : [ DataSourceToIndexFieldMapping, ... ],
  "[InclusionPatterns](#cfn-kendra-datasource-googledriveconfiguration-inclusionpatterns)" : [ String, ... ],
  "[SecretArn](#cfn-kendra-datasource-googledriveconfiguration-secretarn)" : String
}
```

### YAML<a name="aws-properties-kendra-datasource-googledriveconfiguration-syntax.yaml"></a>

```
  [ExcludeMimeTypes](#cfn-kendra-datasource-googledriveconfiguration-excludemimetypes): 
    - String
  [ExcludeSharedDrives](#cfn-kendra-datasource-googledriveconfiguration-excludeshareddrives): 
    - String
  [ExcludeUserAccounts](#cfn-kendra-datasource-googledriveconfiguration-excludeuseraccounts): 
    - String
  [ExclusionPatterns](#cfn-kendra-datasource-googledriveconfiguration-exclusionpatterns): 
    - String
  [FieldMappings](#cfn-kendra-datasource-googledriveconfiguration-fieldmappings): 
    - DataSourceToIndexFieldMapping
  [InclusionPatterns](#cfn-kendra-datasource-googledriveconfiguration-inclusionpatterns): 
    - String
  [SecretArn](#cfn-kendra-datasource-googledriveconfiguration-secretarn): String
```

## Properties<a name="aws-properties-kendra-datasource-googledriveconfiguration-properties"></a>

`ExcludeMimeTypes`  <a name="cfn-kendra-datasource-googledriveconfiguration-excludemimetypes"></a>
A list of MIME types to exclude from the index\. All documents matching the specified MIME type are excluded\.   
For a list of MIME types, see [Using a Google Workspace Drive data source](https://docs.aws.amazon.com/kendra/latest/dg/data-source-google-drive.html)\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `30`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludeSharedDrives`  <a name="cfn-kendra-datasource-googledriveconfiguration-excludeshareddrives"></a>
A list of identifiers or shared drives to exclude from the index\. All files and folders stored on the shared drive are excluded\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludeUserAccounts`  <a name="cfn-kendra-datasource-googledriveconfiguration-excludeuseraccounts"></a>
A list of email addresses of the users\. Documents owned by these users are excluded from the index\. Documents shared with excluded users are indexed unless they are excluded in another way\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExclusionPatterns`  <a name="cfn-kendra-datasource-googledriveconfiguration-exclusionpatterns"></a>
A list of regular expression patterns to exclude certain items in your Google Drive, including shared drives and users' My Drives\. Items that match the patterns are excluded from the index\. Items that don't match the patterns are included in the index\. If an item matches both an inclusion and exclusion pattern, the exclusion pattern takes precedence and the item isn't included in the index\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldMappings`  <a name="cfn-kendra-datasource-googledriveconfiguration-fieldmappings"></a>
Maps Google Drive data source attributes or field names to Amazon Kendra index field names\. To create custom fields, use the `UpdateIndex` API before you map to Google Drive fields\. For more information, see [Mapping data source fields](https://docs.aws.amazon.com/kendra/latest/dg/field-mapping.html)\. The Google Drive data source field names must exist in your Google Drive custom metadata\.  
*Required*: No  
*Type*: List of [DataSourceToIndexFieldMapping](aws-properties-kendra-datasource-datasourcetoindexfieldmapping.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InclusionPatterns`  <a name="cfn-kendra-datasource-googledriveconfiguration-inclusionpatterns"></a>
A list of regular expression patterns to include certain items in your Google Drive, including shared drives and users' My Drives\. Items that match the patterns are included in the index\. Items that don't match the patterns are excluded from the index\. If an item matches both an inclusion and exclusion pattern, the exclusion pattern takes precedence and the item isn't included in the index\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretArn`  <a name="cfn-kendra-datasource-googledriveconfiguration-secretarn"></a>
The Amazon Resource Name \(ARN\) of a AWS Secrets Managersecret that contains the credentials required to connect to Google Drive\. For more information, see [Using a Google Workspace Drive data source](https://docs.aws.amazon.com/kendra/latest/dg/data-source-google-drive.html)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1284`  
*Pattern*: `arn:[a-z0-9-\.]{1,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[^/].{0,1023}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)