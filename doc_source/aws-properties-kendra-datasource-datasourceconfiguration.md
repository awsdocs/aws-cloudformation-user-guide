# AWS::Kendra::DataSource DataSourceConfiguration<a name="aws-properties-kendra-datasource-datasourceconfiguration"></a>

Configuration information for a Amazon Kendra data source\.

## Syntax<a name="aws-properties-kendra-datasource-datasourceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-datasourceconfiguration-syntax.json"></a>

```
{
  "[ConfluenceConfiguration](#cfn-kendra-datasource-datasourceconfiguration-confluenceconfiguration)" : ConfluenceConfiguration,
  "[DatabaseConfiguration](#cfn-kendra-datasource-datasourceconfiguration-databaseconfiguration)" : DatabaseConfiguration,
  "[OneDriveConfiguration](#cfn-kendra-datasource-datasourceconfiguration-onedriveconfiguration)" : OneDriveConfiguration,
  "[S3Configuration](#cfn-kendra-datasource-datasourceconfiguration-s3configuration)" : S3DataSourceConfiguration,
  "[SalesforceConfiguration](#cfn-kendra-datasource-datasourceconfiguration-salesforceconfiguration)" : SalesforceConfiguration,
  "[ServiceNowConfiguration](#cfn-kendra-datasource-datasourceconfiguration-servicenowconfiguration)" : ServiceNowConfiguration,
  "[SharePointConfiguration](#cfn-kendra-datasource-datasourceconfiguration-sharepointconfiguration)" : SharePointConfiguration
}
```

### YAML<a name="aws-properties-kendra-datasource-datasourceconfiguration-syntax.yaml"></a>

```
  [ConfluenceConfiguration](#cfn-kendra-datasource-datasourceconfiguration-confluenceconfiguration): 
    ConfluenceConfiguration
  [DatabaseConfiguration](#cfn-kendra-datasource-datasourceconfiguration-databaseconfiguration): 
    DatabaseConfiguration
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
```

## Properties<a name="aws-properties-kendra-datasource-datasourceconfiguration-properties"></a>

`ConfluenceConfiguration`  <a name="cfn-kendra-datasource-datasourceconfiguration-confluenceconfiguration"></a>
Provides configuration information for connecting to a Confluence data source\.  
*Required*: No  
*Type*: [ConfluenceConfiguration](aws-properties-kendra-datasource-confluenceconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseConfiguration`  <a name="cfn-kendra-datasource-datasourceconfiguration-databaseconfiguration"></a>
Provides information necessary to create a data source connector for a database\.  
*Required*: No  
*Type*: [DatabaseConfiguration](aws-properties-kendra-datasource-databaseconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OneDriveConfiguration`  <a name="cfn-kendra-datasource-datasourceconfiguration-onedriveconfiguration"></a>
Provides configuration for data sources that connect to Microsoft OneDrive\.  
*Required*: No  
*Type*: [OneDriveConfiguration](aws-properties-kendra-datasource-onedriveconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Configuration`  <a name="cfn-kendra-datasource-datasourceconfiguration-s3configuration"></a>
Provides information to create a data source connector for a document repository in an Amazon S3 bucket\.  
*Required*: No  
*Type*: [S3DataSourceConfiguration](aws-properties-kendra-datasource-s3datasourceconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SalesforceConfiguration`  <a name="cfn-kendra-datasource-datasourceconfiguration-salesforceconfiguration"></a>
Provides configuration information for data sources that connect to a Salesforce site\.  
*Required*: No  
*Type*: [SalesforceConfiguration](aws-properties-kendra-datasource-salesforceconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceNowConfiguration`  <a name="cfn-kendra-datasource-datasourceconfiguration-servicenowconfiguration"></a>
Provides configuration for data sources that connect to ServiceNow instances\.  
*Required*: No  
*Type*: [ServiceNowConfiguration](aws-properties-kendra-datasource-servicenowconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SharePointConfiguration`  <a name="cfn-kendra-datasource-datasourceconfiguration-sharepointconfiguration"></a>
Provides information necessary to create a data source connector for a Microsoft SharePoint site\.  
*Required*: No  
*Type*: [SharePointConfiguration](aws-properties-kendra-datasource-sharepointconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)