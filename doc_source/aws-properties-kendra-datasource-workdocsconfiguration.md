# AWS::Kendra::DataSource WorkDocsConfiguration<a name="aws-properties-kendra-datasource-workdocsconfiguration"></a>

Provides the configuration information to connect to Amazon WorkDocs as your data source\.

Amazon WorkDocs connector is available in Oregon, North Virginia, Sydney, Singapore and Ireland regions\.

## Syntax<a name="aws-properties-kendra-datasource-workdocsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-workdocsconfiguration-syntax.json"></a>

```
{
  "[CrawlComments](#cfn-kendra-datasource-workdocsconfiguration-crawlcomments)" : Boolean,
  "[ExclusionPatterns](#cfn-kendra-datasource-workdocsconfiguration-exclusionpatterns)" : [ String, ... ],
  "[FieldMappings](#cfn-kendra-datasource-workdocsconfiguration-fieldmappings)" : [ DataSourceToIndexFieldMapping, ... ],
  "[InclusionPatterns](#cfn-kendra-datasource-workdocsconfiguration-inclusionpatterns)" : [ String, ... ],
  "[OrganizationId](#cfn-kendra-datasource-workdocsconfiguration-organizationid)" : String,
  "[UseChangeLog](#cfn-kendra-datasource-workdocsconfiguration-usechangelog)" : Boolean
}
```

### YAML<a name="aws-properties-kendra-datasource-workdocsconfiguration-syntax.yaml"></a>

```
  [CrawlComments](#cfn-kendra-datasource-workdocsconfiguration-crawlcomments): Boolean
  [ExclusionPatterns](#cfn-kendra-datasource-workdocsconfiguration-exclusionpatterns): 
    - String
  [FieldMappings](#cfn-kendra-datasource-workdocsconfiguration-fieldmappings): 
    - DataSourceToIndexFieldMapping
  [InclusionPatterns](#cfn-kendra-datasource-workdocsconfiguration-inclusionpatterns): 
    - String
  [OrganizationId](#cfn-kendra-datasource-workdocsconfiguration-organizationid): String
  [UseChangeLog](#cfn-kendra-datasource-workdocsconfiguration-usechangelog): Boolean
```

## Properties<a name="aws-properties-kendra-datasource-workdocsconfiguration-properties"></a>

`CrawlComments`  <a name="cfn-kendra-datasource-workdocsconfiguration-crawlcomments"></a>
 `TRUE` to include comments on documents in your index\. Including comments in your index means each comment is a document that can be searched on\.  
The default is set to `FALSE`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExclusionPatterns`  <a name="cfn-kendra-datasource-workdocsconfiguration-exclusionpatterns"></a>
A list of regular expression patterns to exclude certain files in your Amazon WorkDocs site repository\. Files that match the patterns are excluded from the index\. Files that don’t match the patterns are included in the index\. If a file matches both an inclusion and exclusion pattern, the exclusion pattern takes precedence and the file isn't included in the index\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldMappings`  <a name="cfn-kendra-datasource-workdocsconfiguration-fieldmappings"></a>
A list of `DataSourceToIndexFieldMapping` objects that map Amazon WorkDocs data source attributes or field names to Amazon Kendra index field names\. To create custom fields, use the `UpdateIndex` API before you map to Amazon WorkDocs fields\. For more information, see [Mapping data source fields](https://docs.aws.amazon.com/kendra/latest/dg/field-mapping.html)\. The Amazon WorkDocs data source field names must exist in your Amazon WorkDocs custom metadata\.  
*Required*: No  
*Type*: List of [DataSourceToIndexFieldMapping](aws-properties-kendra-datasource-datasourcetoindexfieldmapping.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InclusionPatterns`  <a name="cfn-kendra-datasource-workdocsconfiguration-inclusionpatterns"></a>
A list of regular expression patterns to include certain files in your Amazon WorkDocs site repository\. Files that match the patterns are included in the index\. Files that don't match the patterns are excluded from the index\. If a file matches both an inclusion and exclusion pattern, the exclusion pattern takes precedence and the file isn't included in the index\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OrganizationId`  <a name="cfn-kendra-datasource-workdocsconfiguration-organizationid"></a>
The identifier of the directory corresponding to your Amazon WorkDocs site repository\.  
You can find the organization ID in the [AWS Directory Service](https://console.aws.amazon.com/directoryservicev2/) by going to **Active Directory**, then **Directories**\. Your Amazon WorkDocs site directory has an ID, which is the organization ID\. You can also set up a new Amazon WorkDocs directory in the AWS Directory Service console and enable a Amazon WorkDocs site for the directory in the Amazon WorkDocs console\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `12`  
*Maximum*: `12`  
*Pattern*: `d-[0-9a-fA-F]{10}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseChangeLog`  <a name="cfn-kendra-datasource-workdocsconfiguration-usechangelog"></a>
 `TRUE` to use the Amazon WorkDocs change log to determine which documents require updating in the index\. Depending on the change log's size, it may take longer for Amazon Kendra to use the change log than to scan all of your documents in Amazon WorkDocs\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)