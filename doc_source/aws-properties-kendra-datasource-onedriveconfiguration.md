# AWS::Kendra::DataSource OneDriveConfiguration<a name="aws-properties-kendra-datasource-onedriveconfiguration"></a>

Provides configuration information for data sources that connect to OneDrive\.

## Syntax<a name="aws-properties-kendra-datasource-onedriveconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-onedriveconfiguration-syntax.json"></a>

```
{
  "[DisableLocalGroups](#cfn-kendra-datasource-onedriveconfiguration-disablelocalgroups)" : Boolean,
  "[ExclusionPatterns](#cfn-kendra-datasource-onedriveconfiguration-exclusionpatterns)" : DataSourceInclusionsExclusionsStrings,
  "[FieldMappings](#cfn-kendra-datasource-onedriveconfiguration-fieldmappings)" : DataSourceToIndexFieldMappingList,
  "[InclusionPatterns](#cfn-kendra-datasource-onedriveconfiguration-inclusionpatterns)" : DataSourceInclusionsExclusionsStrings,
  "[OneDriveUsers](#cfn-kendra-datasource-onedriveconfiguration-onedriveusers)" : OneDriveUsers,
  "[SecretArn](#cfn-kendra-datasource-onedriveconfiguration-secretarn)" : String,
  "[TenantDomain](#cfn-kendra-datasource-onedriveconfiguration-tenantdomain)" : String
}
```

### YAML<a name="aws-properties-kendra-datasource-onedriveconfiguration-syntax.yaml"></a>

```
  [DisableLocalGroups](#cfn-kendra-datasource-onedriveconfiguration-disablelocalgroups): Boolean
  [ExclusionPatterns](#cfn-kendra-datasource-onedriveconfiguration-exclusionpatterns): 
    DataSourceInclusionsExclusionsStrings
  [FieldMappings](#cfn-kendra-datasource-onedriveconfiguration-fieldmappings): 
    DataSourceToIndexFieldMappingList
  [InclusionPatterns](#cfn-kendra-datasource-onedriveconfiguration-inclusionpatterns): 
    DataSourceInclusionsExclusionsStrings
  [OneDriveUsers](#cfn-kendra-datasource-onedriveconfiguration-onedriveusers): 
    OneDriveUsers
  [SecretArn](#cfn-kendra-datasource-onedriveconfiguration-secretarn): String
  [TenantDomain](#cfn-kendra-datasource-onedriveconfiguration-tenantdomain): String
```

## Properties<a name="aws-properties-kendra-datasource-onedriveconfiguration-properties"></a>

`DisableLocalGroups`  <a name="cfn-kendra-datasource-onedriveconfiguration-disablelocalgroups"></a>
A Boolean value that specifies whether local groups are disabled \(`True`\) or enabled \(`False`\)\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExclusionPatterns`  <a name="cfn-kendra-datasource-onedriveconfiguration-exclusionpatterns"></a>
List of regular expressions applied to documents\. Items that match the exclusion pattern are not indexed\. If you provide both an inclusion pattern and an exclusion pattern, any item that matches the exclusion pattern isn't indexed\.   
The exclusion pattern is applied to the file name\.  
*Required*: No  
*Type*: [DataSourceInclusionsExclusionsStrings](aws-properties-kendra-datasource-datasourceinclusionsexclusionsstrings.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldMappings`  <a name="cfn-kendra-datasource-onedriveconfiguration-fieldmappings"></a>
A list of `DataSourceToIndexFieldMapping` objects that map Microsoft OneDrive fields to custom fields in the Amazon Kendra index\. You must first create the index fields before you map OneDrive fields\.  
*Required*: No  
*Type*: [DataSourceToIndexFieldMappingList](aws-properties-kendra-datasource-datasourcetoindexfieldmappinglist.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InclusionPatterns`  <a name="cfn-kendra-datasource-onedriveconfiguration-inclusionpatterns"></a>
A list of regular expression patterns\. Documents that match the pattern are included in the index\. Documents that don't match the pattern are excluded from the index\. If a document matches both an inclusion pattern and an exclusion pattern, the document is not included in the index\.   
The exclusion pattern is applied to the file name\.  
*Required*: No  
*Type*: [DataSourceInclusionsExclusionsStrings](aws-properties-kendra-datasource-datasourceinclusionsexclusionsstrings.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OneDriveUsers`  <a name="cfn-kendra-datasource-onedriveconfiguration-onedriveusers"></a>
A list of user accounts whose documents should be indexed\.  
*Required*: Yes  
*Type*: [OneDriveUsers](aws-properties-kendra-datasource-onedriveusers.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretArn`  <a name="cfn-kendra-datasource-onedriveconfiguration-secretarn"></a>
The Amazon Resource Name \(ARN\) of an AWS Secrets Manager secret that contains the user name and password to connect to OneDrive\. The user named should be the application ID for the OneDrive application, and the password is the application key for the OneDrive application\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1284`  
*Pattern*: `arn:[a-z0-9-\.]{1,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[^/].{0,1023}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TenantDomain`  <a name="cfn-kendra-datasource-onedriveconfiguration-tenantdomain"></a>
The Azure Active Directory domain of the organization\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^([a-zA-Z0-9]+(-[a-zA-Z0-9]+)*\.)+[a-z]{2,}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)