# AWS::Kendra::DataSource DataSourceConfiguration<a name="aws-properties-kendra-datasource-datasourceconfiguration"></a>

Provides the configuration information for an Amazon Kendra data source\.

## Syntax<a name="aws-properties-kendra-datasource-datasourceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-datasourceconfiguration-syntax.json"></a>

```
{
  "[ConfluenceConfiguration](#cfn-kendra-datasource-datasourceconfiguration-confluenceconfiguration)" : ConfluenceConfiguration,
  "[DatabaseConfiguration](#cfn-kendra-datasource-datasourceconfiguration-databaseconfiguration)" : DatabaseConfiguration,
  "[GoogleDriveConfiguration](#cfn-kendra-datasource-datasourceconfiguration-googledriveconfiguration)" : GoogleDriveConfiguration,
  "[OneDriveConfiguration](#cfn-kendra-datasource-datasourceconfiguration-onedriveconfiguration)" : OneDriveConfiguration,
  "[S3Configuration](#cfn-kendra-datasource-datasourceconfiguration-s3configuration)" : S3DataSourceConfiguration,
  "[SalesforceConfiguration](#cfn-kendra-datasource-datasourceconfiguration-salesforceconfiguration)" : SalesforceConfiguration,
  "[ServiceNowConfiguration](#cfn-kendra-datasource-datasourceconfiguration-servicenowconfiguration)" : ServiceNowConfiguration,
  "[SharePointConfiguration](#cfn-kendra-datasource-datasourceconfiguration-sharepointconfiguration)" : SharePointConfiguration,
  "[WebCrawlerConfiguration](#cfn-kendra-datasource-datasourceconfiguration-webcrawlerconfiguration)" : WebCrawlerConfiguration,
  "[WorkDocsConfiguration](#cfn-kendra-datasource-datasourceconfiguration-workdocsconfiguration)" : WorkDocsConfiguration
}
```

### YAML<a name="aws-properties-kendra-datasource-datasourceconfiguration-syntax.yaml"></a>

```
  [ConfluenceConfiguration](#cfn-kendra-datasource-datasourceconfiguration-confluenceconfiguration): 
    ConfluenceConfiguration
  [DatabaseConfiguration](#cfn-kendra-datasource-datasourceconfiguration-databaseconfiguration): 
    DatabaseConfiguration
  [GoogleDriveConfiguration](#cfn-kendra-datasource-datasourceconfiguration-googledriveconfiguration): 
    GoogleDriveConfiguration
  [OneDriveConfiguration](#cfn-kendra-datasource-datasourceconfiguration-onedriveconfiguration): 
    OneDriveConfiguration
  [S3Configuration](#cfn-kendra-datasource-datasourceconfiguration-s3configuration): 
    S3DataSourceConfiguration
  [SalesforceConfiguration](#cfn-kendra-datasource-datasourceconfiguration-salesforceconfiguration): 
    SalesforceConfiguration
  [ServiceNowConfiguration](#cfn-kendra-datasource-datasourceconfiguration-servicenowconfiguration): 
    ServiceNowConfiguration
  [SharePointConfiguration](#cfn-kendra-datasource-datasourceconfiguration-sharepointconfiguration): 
    SharePointConfiguration
  [WebCrawlerConfiguration](#cfn-kendra-datasource-datasourceconfiguration-webcrawlerconfiguration): 
    WebCrawlerConfiguration
  [WorkDocsConfiguration](#cfn-kendra-datasource-datasourceconfiguration-workdocsconfiguration): 
    WorkDocsConfiguration
```

## Properties<a name="aws-properties-kendra-datasource-datasourceconfiguration-properties"></a>

`ConfluenceConfiguration`  <a name="cfn-kendra-datasource-datasourceconfiguration-confluenceconfiguration"></a>
Provides the configuration information to connect to Confluence as your data source\.  
*Required*: No  
*Type*: [ConfluenceConfiguration](aws-properties-kendra-datasource-confluenceconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseConfiguration`  <a name="cfn-kendra-datasource-datasourceconfiguration-databaseconfiguration"></a>
Provides the configuration information to connect to a database as your data source\.  
*Required*: No  
*Type*: [DatabaseConfiguration](aws-properties-kendra-datasource-databaseconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GoogleDriveConfiguration`  <a name="cfn-kendra-datasource-datasourceconfiguration-googledriveconfiguration"></a>
Provides the configuration information to connect to Google Drive as your data source\.  
*Required*: No  
*Type*: [GoogleDriveConfiguration](aws-properties-kendra-datasource-googledriveconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OneDriveConfiguration`  <a name="cfn-kendra-datasource-datasourceconfiguration-onedriveconfiguration"></a>
Provides the configuration information to connect to Microsoft OneDrive as your data source\.  
*Required*: No  
*Type*: [OneDriveConfiguration](aws-properties-kendra-datasource-onedriveconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Configuration`  <a name="cfn-kendra-datasource-datasourceconfiguration-s3configuration"></a>
Provides the configuration information to connect to an Amazon S3 bucket as your data source\.  
*Required*: No  
*Type*: [S3DataSourceConfiguration](aws-properties-kendra-datasource-s3datasourceconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SalesforceConfiguration`  <a name="cfn-kendra-datasource-datasourceconfiguration-salesforceconfiguration"></a>
Provides the configuration information to connect to Salesforce as your data source\.  
*Required*: No  
*Type*: [SalesforceConfiguration](aws-properties-kendra-datasource-salesforceconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceNowConfiguration`  <a name="cfn-kendra-datasource-datasourceconfiguration-servicenowconfiguration"></a>
Provides the configuration information to connect to ServiceNow as your data source\.  
*Required*: No  
*Type*: [ServiceNowConfiguration](aws-properties-kendra-datasource-servicenowconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SharePointConfiguration`  <a name="cfn-kendra-datasource-datasourceconfiguration-sharepointconfiguration"></a>
Provides the configuration information to connect to Microsoft SharePoint as your data source\.  
*Required*: No  
*Type*: [SharePointConfiguration](aws-properties-kendra-datasource-sharepointconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WebCrawlerConfiguration`  <a name="cfn-kendra-datasource-datasourceconfiguration-webcrawlerconfiguration"></a>
Provides the configuration information required for Amazon Kendra Web Crawler\.  
*Required*: No  
*Type*: [WebCrawlerConfiguration](aws-properties-kendra-datasource-webcrawlerconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WorkDocsConfiguration`  <a name="cfn-kendra-datasource-datasourceconfiguration-workdocsconfiguration"></a>
Provides the configuration information to connect to Amazon WorkDocs as your data source\.  
*Required*: No  
*Type*: [WorkDocsConfiguration](aws-properties-kendra-datasource-workdocsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)