# AWS::Kendra::DataSource OneDriveConfiguration<a name="aws-properties-kendra-datasource-onedriveconfiguration"></a>

Provides the configuration information to connect to OneDrive as your data source\.

## Syntax<a name="aws-properties-kendra-datasource-onedriveconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-onedriveconfiguration-syntax.json"></a>

```
{
  "[DisableLocalGroups](#cfn-kendra-datasource-onedriveconfiguration-disablelocalgroups)" : Boolean,
  "[ExclusionPatterns](#cfn-kendra-datasource-onedriveconfiguration-exclusionpatterns)" : [ String, ... ],
  "[FieldMappings](#cfn-kendra-datasource-onedriveconfiguration-fieldmappings)" : [ DataSourceToIndexFieldMapping, ... ],
  "[InclusionPatterns](#cfn-kendra-datasource-onedriveconfiguration-inclusionpatterns)" : [ String, ... ],
  "[OneDriveUsers](#cfn-kendra-datasource-onedriveconfiguration-onedriveusers)" : OneDriveUsers,
  "[SecretArn](#cfn-kendra-datasource-onedriveconfiguration-secretarn)" : String,
  "[TenantDomain](#cfn-kendra-datasource-onedriveconfiguration-tenantdomain)" : String
}
```

### YAML<a name="aws-properties-kendra-datasource-onedriveconfiguration-syntax.yaml"></a>

```
  [DisableLocalGroups](#cfn-kendra-datasource-onedriveconfiguration-disablelocalgroups): Boolean
  [ExclusionPatterns](#cfn-kendra-datasource-onedriveconfiguration-exclusionpatterns): 
    - String
  [FieldMappings](#cfn-kendra-datasource-onedriveconfiguration-fieldmappings): 
    - DataSourceToIndexFieldMapping
  [InclusionPatterns](#cfn-kendra-datasource-onedriveconfiguration-inclusionpatterns): 
    - String
  [OneDriveUsers](#cfn-kendra-datasource-onedriveconfiguration-onedriveusers): 
    OneDriveUsers
  [SecretArn](#cfn-kendra-datasource-onedriveconfiguration-secretarn): String
  [TenantDomain](#cfn-kendra-datasource-onedriveconfiguration-tenantdomain): String
```

## Properties<a name="aws-properties-kendra-datasource-onedriveconfiguration-properties"></a>

`DisableLocalGroups`  <a name="cfn-kendra-datasource-onedriveconfiguration-disablelocalgroups"></a>
 `TRUE` to disable local groups information\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExclusionPatterns`  <a name="cfn-kendra-datasource-onedriveconfiguration-exclusionpatterns"></a>
A list of regular expression patterns to exclude certain documents in your OneDrive\. Documents that match the patterns are excluded from the index\. Documents that don't match the patterns are included in the index\. If a document matches both an inclusion and exclusion pattern, the exclusion pattern takes precedence and the document isn't included in the index\.  
The pattern is applied to the file name\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldMappings`  <a name="cfn-kendra-datasource-onedriveconfiguration-fieldmappings"></a>
A list of `DataSourceToIndexFieldMapping` objects that map OneDrive data source attributes or field names to Amazon Kendra index field names\. To create custom fields, use the `UpdateIndex` API before you map to OneDrive fields\. For more information, see [Mapping data source fields](https://docs.aws.amazon.com/kendra/latest/dg/field-mapping.html)\. The OneDrive data source field names must exist in your OneDrive custom metadata\.  
*Required*: No  
*Type*: List of [DataSourceToIndexFieldMapping](aws-properties-kendra-datasource-datasourcetoindexfieldmapping.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InclusionPatterns`  <a name="cfn-kendra-datasource-onedriveconfiguration-inclusionpatterns"></a>
A list of regular expression patterns to include certain documents in your OneDrive\. Documents that match the patterns are included in the index\. Documents that don't match the patterns are excluded from the index\. If a document matches both an inclusion and exclusion pattern, the exclusion pattern takes precedence and the document isn't included in the index\.  
The pattern is applied to the file name\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OneDriveUsers`  <a name="cfn-kendra-datasource-onedriveconfiguration-onedriveusers"></a>
A list of user accounts whose documents should be indexed\.  
*Required*: Yes  
*Type*: [OneDriveUsers](aws-properties-kendra-datasource-onedriveusers.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretArn`  <a name="cfn-kendra-datasource-onedriveconfiguration-secretarn"></a>
The Amazon Resource Name \(ARN\) of an AWS Secrets Manager secret that contains the user name and password to connect to OneDrive\. The user name should be the application ID for the OneDrive application, and the password is the application key for the OneDrive application\.  
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