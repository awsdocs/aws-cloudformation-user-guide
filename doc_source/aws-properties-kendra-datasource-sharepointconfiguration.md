# AWS::Kendra::DataSource SharePointConfiguration<a name="aws-properties-kendra-datasource-sharepointconfiguration"></a>

Provides the configuration information to connect to Microsoft SharePoint as your data source\.

## Syntax<a name="aws-properties-kendra-datasource-sharepointconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-sharepointconfiguration-syntax.json"></a>

```
{
  "[CrawlAttachments](#cfn-kendra-datasource-sharepointconfiguration-crawlattachments)" : Boolean,
  "[DisableLocalGroups](#cfn-kendra-datasource-sharepointconfiguration-disablelocalgroups)" : Boolean,
  "[DocumentTitleFieldName](#cfn-kendra-datasource-sharepointconfiguration-documenttitlefieldname)" : String,
  "[ExclusionPatterns](#cfn-kendra-datasource-sharepointconfiguration-exclusionpatterns)" : [ String, ... ],
  "[FieldMappings](#cfn-kendra-datasource-sharepointconfiguration-fieldmappings)" : [ DataSourceToIndexFieldMapping, ... ],
  "[InclusionPatterns](#cfn-kendra-datasource-sharepointconfiguration-inclusionpatterns)" : [ String, ... ],
  "[SecretArn](#cfn-kendra-datasource-sharepointconfiguration-secretarn)" : String,
  "[SharePointVersion](#cfn-kendra-datasource-sharepointconfiguration-sharepointversion)" : String,
  "[SslCertificateS3Path](#cfn-kendra-datasource-sharepointconfiguration-sslcertificates3path)" : S3Path,
  "[Urls](#cfn-kendra-datasource-sharepointconfiguration-urls)" : [ String, ... ],
  "[UseChangeLog](#cfn-kendra-datasource-sharepointconfiguration-usechangelog)" : Boolean,
  "[VpcConfiguration](#cfn-kendra-datasource-sharepointconfiguration-vpcconfiguration)" : DataSourceVpcConfiguration
}
```

### YAML<a name="aws-properties-kendra-datasource-sharepointconfiguration-syntax.yaml"></a>

```
  [CrawlAttachments](#cfn-kendra-datasource-sharepointconfiguration-crawlattachments): Boolean
  [DisableLocalGroups](#cfn-kendra-datasource-sharepointconfiguration-disablelocalgroups): Boolean
  [DocumentTitleFieldName](#cfn-kendra-datasource-sharepointconfiguration-documenttitlefieldname): String
  [ExclusionPatterns](#cfn-kendra-datasource-sharepointconfiguration-exclusionpatterns): 
    - String
  [FieldMappings](#cfn-kendra-datasource-sharepointconfiguration-fieldmappings): 
    - DataSourceToIndexFieldMapping
  [InclusionPatterns](#cfn-kendra-datasource-sharepointconfiguration-inclusionpatterns): 
    - String
  [SecretArn](#cfn-kendra-datasource-sharepointconfiguration-secretarn): String
  [SharePointVersion](#cfn-kendra-datasource-sharepointconfiguration-sharepointversion): String
  [SslCertificateS3Path](#cfn-kendra-datasource-sharepointconfiguration-sslcertificates3path): 
    S3Path
  [Urls](#cfn-kendra-datasource-sharepointconfiguration-urls): 
    - String
  [UseChangeLog](#cfn-kendra-datasource-sharepointconfiguration-usechangelog): Boolean
  [VpcConfiguration](#cfn-kendra-datasource-sharepointconfiguration-vpcconfiguration): 
    DataSourceVpcConfiguration
```

## Properties<a name="aws-properties-kendra-datasource-sharepointconfiguration-properties"></a>

`CrawlAttachments`  <a name="cfn-kendra-datasource-sharepointconfiguration-crawlattachments"></a>
 `TRUE` to index document attachments\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisableLocalGroups`  <a name="cfn-kendra-datasource-sharepointconfiguration-disablelocalgroups"></a>
 `TRUE` to disable local groups information\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentTitleFieldName`  <a name="cfn-kendra-datasource-sharepointconfiguration-documenttitlefieldname"></a>
The Microsoft SharePoint attribute field that contains the title of the document\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_.]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExclusionPatterns`  <a name="cfn-kendra-datasource-sharepointconfiguration-exclusionpatterns"></a>
A list of regular expression patterns\. Documents that match the patterns are excluded from the index\. Documents that don't match the patterns are included in the index\. If a document matches both an exclusion pattern and an inclusion pattern, the document is not included in the index\.  
The regex is applied to the display URL of the SharePoint document\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldMappings`  <a name="cfn-kendra-datasource-sharepointconfiguration-fieldmappings"></a>
A list of `DataSourceToIndexFieldMapping` objects that map Microsoft SharePoint attributes or fields to Amazon Kendra index fields\. You must first create the index fields using the [UpdateIndex](https://docs.aws.amazon.com/kendra/latest/dg/API_UpdateIndex.html) operation before you map SharePoint attributes\. For more information, see [Mapping Data Source Fields](https://docs.aws.amazon.com/kendra/latest/dg/field-mapping.html)\.  
*Required*: No  
*Type*: List of [DataSourceToIndexFieldMapping](aws-properties-kendra-datasource-datasourcetoindexfieldmapping.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InclusionPatterns`  <a name="cfn-kendra-datasource-sharepointconfiguration-inclusionpatterns"></a>
A list of regular expression patterns to include certain documents in your SharePoint\. Documents that match the patterns are included in the index\. Documents that don't match the patterns are excluded from the index\. If a document matches both an inclusion and exclusion pattern, the exclusion pattern takes precedence and the document isn't included in the index\.  
The regex applies to the display URL of the SharePoint document\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretArn`  <a name="cfn-kendra-datasource-sharepointconfiguration-secretarn"></a>
The Amazon Resource Name \(ARN\) of an AWS Secrets Manager secret that contains the user name and password required to connect to the SharePoint instance\. For more information, see [Microsoft SharePoint](https://docs.aws.amazon.com/kendra/latest/dg/data-source-sharepoint.html)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1284`  
*Pattern*: `arn:[a-z0-9-\.]{1,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[^/].{0,1023}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SharePointVersion`  <a name="cfn-kendra-datasource-sharepointconfiguration-sharepointversion"></a>
The version of Microsoft SharePoint that you use\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `SHAREPOINT_2013 | SHAREPOINT_2016 | SHAREPOINT_2019 | SHAREPOINT_ONLINE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SslCertificateS3Path`  <a name="cfn-kendra-datasource-sharepointconfiguration-sslcertificates3path"></a>
Information required to find a specific file in an Amazon S3 bucket\.  
*Required*: No  
*Type*: [S3Path](aws-properties-kendra-datasource-s3path.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Urls`  <a name="cfn-kendra-datasource-sharepointconfiguration-urls"></a>
The Microsoft SharePoint site URLs for the documents you want to index\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseChangeLog`  <a name="cfn-kendra-datasource-sharepointconfiguration-usechangelog"></a>
 `TRUE` to use the SharePoint change log to determine which documents require updating in the index\. Depending on the change log's size, it may take longer for Amazon Kendra to use the change log than to scan all of your documents in SharePoint\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcConfiguration`  <a name="cfn-kendra-datasource-sharepointconfiguration-vpcconfiguration"></a>
Provides information for connecting to an Amazon VPC\.  
*Required*: No  
*Type*: [DataSourceVpcConfiguration](aws-properties-kendra-datasource-datasourcevpcconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)