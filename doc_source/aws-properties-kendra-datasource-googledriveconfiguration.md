# AWS::Kendra::DataSource GoogleDriveConfiguration<a name="aws-properties-kendra-datasource-googledriveconfiguration"></a>

Provides configuration information for data sources that connect to Google Drive\.

## Syntax<a name="aws-properties-kendra-datasource-googledriveconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-googledriveconfiguration-syntax.json"></a>

```
{
  "[ExcludeMimeTypes](#cfn-kendra-datasource-googledriveconfiguration-excludemimetypes)" : ExcludeMimeTypesList,
  "[ExcludeSharedDrives](#cfn-kendra-datasource-googledriveconfiguration-excludeshareddrives)" : ExcludeSharedDrivesList,
  "[ExcludeUserAccounts](#cfn-kendra-datasource-googledriveconfiguration-excludeuseraccounts)" : ExcludeUserAccountsList,
  "[ExclusionPatterns](#cfn-kendra-datasource-googledriveconfiguration-exclusionpatterns)" : DataSourceInclusionsExclusionsStrings,
  "[FieldMappings](#cfn-kendra-datasource-googledriveconfiguration-fieldmappings)" : DataSourceToIndexFieldMappingList,
  "[InclusionPatterns](#cfn-kendra-datasource-googledriveconfiguration-inclusionpatterns)" : DataSourceInclusionsExclusionsStrings,
  "[SecretArn](#cfn-kendra-datasource-googledriveconfiguration-secretarn)" : String
}
```

### YAML<a name="aws-properties-kendra-datasource-googledriveconfiguration-syntax.yaml"></a>

```
  [ExcludeMimeTypes](#cfn-kendra-datasource-googledriveconfiguration-excludemimetypes): 
    ExcludeMimeTypesList
  [ExcludeSharedDrives](#cfn-kendra-datasource-googledriveconfiguration-excludeshareddrives): 
    ExcludeSharedDrivesList
  [ExcludeUserAccounts](#cfn-kendra-datasource-googledriveconfiguration-excludeuseraccounts): 
    ExcludeUserAccountsList
  [ExclusionPatterns](#cfn-kendra-datasource-googledriveconfiguration-exclusionpatterns): 
    DataSourceInclusionsExclusionsStrings
  [FieldMappings](#cfn-kendra-datasource-googledriveconfiguration-fieldmappings): 
    DataSourceToIndexFieldMappingList
  [InclusionPatterns](#cfn-kendra-datasource-googledriveconfiguration-inclusionpatterns): 
    DataSourceInclusionsExclusionsStrings
  [SecretArn](#cfn-kendra-datasource-googledriveconfiguration-secretarn): String
```

## Properties<a name="aws-properties-kendra-datasource-googledriveconfiguration-properties"></a>

`ExcludeMimeTypes`  <a name="cfn-kendra-datasource-googledriveconfiguration-excludemimetypes"></a>
A list of MIME types to exclude from the index\. All documents matching the specified MIME type are excluded\.   
For a list of MIME types, see [Using a Google Workspace Drive data source](https://docs.aws.amazon.com/kendra/latest/dg/data-source-google-drive.html)\.  
*Required*: No  
*Type*: [ExcludeMimeTypesList](aws-properties-kendra-datasource-excludemimetypeslist.md)  
*Maximum*: `30`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludeSharedDrives`  <a name="cfn-kendra-datasource-googledriveconfiguration-excludeshareddrives"></a>
A list of identifiers or shared drives to exclude from the index\. All files and folders stored on the shared drive are excluded\.  
*Required*: No  
*Type*: [ExcludeSharedDrivesList](aws-properties-kendra-datasource-excludeshareddriveslist.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludeUserAccounts`  <a name="cfn-kendra-datasource-googledriveconfiguration-excludeuseraccounts"></a>
A list of email addresses of the users\. Documents owned by these users are excluded from the index\. Documents shared with excluded users are indexed unless they are excluded in another way\.  
*Required*: No  
*Type*: [ExcludeUserAccountsList](aws-properties-kendra-datasource-excludeuseraccountslist.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExclusionPatterns`  <a name="cfn-kendra-datasource-googledriveconfiguration-exclusionpatterns"></a>
A list of regular expression patterns that apply to the path on Google Drive\. Items that match the pattern are excluded from the index from both shared drives and users' My Drives\. Items that don't match the pattern are included in the index\. If an item matches both an exclusion pattern and an inclusion pattern, it is excluded from the index\.  
*Required*: No  
*Type*: [DataSourceInclusionsExclusionsStrings](aws-properties-kendra-datasource-datasourceinclusionsexclusionsstrings.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldMappings`  <a name="cfn-kendra-datasource-googledriveconfiguration-fieldmappings"></a>
Defines mapping between a field in the Google Drive and a Amazon Kendra index field\.  
If you are using the console, you can define index fields when creating the mapping\. If you are using the API, you must first create the field using the UpdateIndex operation\.  
*Required*: No  
*Type*: [DataSourceToIndexFieldMappingList](aws-properties-kendra-datasource-datasourcetoindexfieldmappinglist.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InclusionPatterns`  <a name="cfn-kendra-datasource-googledriveconfiguration-inclusionpatterns"></a>
A list of regular expression patterns that apply to path on Google Drive\. Items that match the pattern are included in the index from both shared drives and users' My Drives\. Items that don't match the pattern are excluded from the index\. If an item matches both an inclusion pattern and an exclusion pattern, it is excluded from the index\.  
*Required*: No  
*Type*: [DataSourceInclusionsExclusionsStrings](aws-properties-kendra-datasource-datasourceinclusionsexclusionsstrings.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretArn`  <a name="cfn-kendra-datasource-googledriveconfiguration-secretarn"></a>
The Amazon Resource Name \(ARN\) of a AWS Secrets Manager secret that contains the credentials required to connect to Google Drive\. For more information, see [Using a Google Workspace Drive data source](https://docs.aws.amazon.com/kendra/latest/dg/data-source-google-drive.html)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1284`  
*Pattern*: `arn:[a-z0-9-\.]{1,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[^/].{0,1023}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)