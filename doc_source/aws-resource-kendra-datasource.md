# AWS::Kendra::DataSource<a name="aws-resource-kendra-datasource"></a>

Specifies a data source that you use to with an Amazon Kendra index\. 

You specify a name, connector type and description for your data source\.

## Syntax<a name="aws-resource-kendra-datasource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-kendra-datasource-syntax.json"></a>

```
{
  "Type" : "AWS::Kendra::DataSource",
  "Properties" : {
      "[DataSourceConfiguration](#cfn-kendra-datasource-datasourceconfiguration)" : DataSourceConfiguration,
      "[Description](#cfn-kendra-datasource-description)" : String,
      "[IndexId](#cfn-kendra-datasource-indexid)" : String,
      "[Name](#cfn-kendra-datasource-name)" : String,
      "[RoleArn](#cfn-kendra-datasource-rolearn)" : String,
      "[Schedule](#cfn-kendra-datasource-schedule)" : String,
      "[Tags](#cfn-kendra-datasource-tags)" : TagList,
      "[Type](#cfn-kendra-datasource-type)" : String
    }
}
```

### YAML<a name="aws-resource-kendra-datasource-syntax.yaml"></a>

```
Type: AWS::Kendra::DataSource
Properties: 
  [DataSourceConfiguration](#cfn-kendra-datasource-datasourceconfiguration): 
    DataSourceConfiguration
  [Description](#cfn-kendra-datasource-description): String
  [IndexId](#cfn-kendra-datasource-indexid): String
  [Name](#cfn-kendra-datasource-name): String
  [RoleArn](#cfn-kendra-datasource-rolearn): String
  [Schedule](#cfn-kendra-datasource-schedule): String
  [Tags](#cfn-kendra-datasource-tags): 
    TagList
  [Type](#cfn-kendra-datasource-type): String
```

## Properties<a name="aws-resource-kendra-datasource-properties"></a>

`DataSourceConfiguration`  <a name="cfn-kendra-datasource-datasourceconfiguration"></a>
Configuration information for an Amazon Kendra data source\. The contents of the configuration depend on the type of data source\. You can only specify one type of data source in the configuration\. Choose from one of the following data sources\.  
+ Amazon S3
+ Confluence
+ Custom
+ Database
+ Microsoft OneDrive
+ Microsoft SharePoint 
+ Salesforce
+ ServiceNow
You can't specify the `Configuration` parameter when the `Type` parameter is set to `CUSTOM`\.  
The `Configuration` parameter is required for all other data sources\.  
*Required*: No  
*Type*: [DataSourceConfiguration](aws-properties-kendra-datasource-datasourceconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-kendra-datasource-description"></a>
A description of the data source\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IndexId`  <a name="cfn-kendra-datasource-indexid"></a>
The identifier of the index that should be associated with this data source\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-kendra-datasource-name"></a>
The name of the data source\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1000`  
*Pattern*: `[a-zA-Z0-9][a-zA-Z0-9_-]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-kendra-datasource-rolearn"></a>
The Amazon Resource Name \(ARN\) of a role with permission to access the data source\.  
You can't specify the `RoleArn` parameter when the `Type` parameter is set to `CUSTOM`\.  
The `RoleArn` parameter is required for all other data sources\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Schedule`  <a name="cfn-kendra-datasource-schedule"></a>
Sets the frequency that Amazon Kendra checks the documents in your data source and updates the index\. If you don't set a schedule, Amazon Kendra doesn't periodically update the index\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-kendra-datasource-tags"></a>
An array of key\-value pairs to apply to this resource  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: [TagList](aws-properties-kendra-datasource-taglist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-kendra-datasource-type"></a>
The type of the data source\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CONFLUENCE | CUSTOM | DATABASE | GOOGLEDRIVE | ONEDRIVE | S3 | SALESFORCE | SERVICENOW | SHAREPOINT`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-kendra-datasource-return-values"></a>

### Ref<a name="aws-resource-kendra-datasource-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the data source ID\. For example:

 `{ "Ref": "<data source ID>|<index ID>" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-kendra-datasource-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-kendra-datasource-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the data source\. For example:  
`arn:aws:kendra:us-west-2:111122223333:index/335c3741-41df-46a6-b5d3-61f85b787884/data-source/b8cae438-6787-4091-8897-684a652bbb0a`

`Id`  <a name="Id-fn::getatt"></a>
The identifier for the data source\. For example:  
 `b8cae438-6787-4091-8897-684a652bbb0a`\.