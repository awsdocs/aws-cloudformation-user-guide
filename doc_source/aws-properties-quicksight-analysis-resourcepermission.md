# AWS::QuickSight::Analysis ResourcePermission<a name="aws-properties-quicksight-analysis-resourcepermission"></a>

Permission for the resource\.

## Syntax<a name="aws-properties-quicksight-analysis-resourcepermission-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-resourcepermission-syntax.json"></a>

```
{
  "[Actions](#cfn-quicksight-analysis-resourcepermission-actions)" : [ String, ... ],
  "[Principal](#cfn-quicksight-analysis-resourcepermission-principal)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-resourcepermission-syntax.yaml"></a>

```
  [Actions](#cfn-quicksight-analysis-resourcepermission-actions): 
    - String
  [Principal](#cfn-quicksight-analysis-resourcepermission-principal): String
```

## Properties<a name="aws-properties-quicksight-analysis-resourcepermission-properties"></a>

`Actions`  <a name="cfn-quicksight-analysis-resourcepermission-actions"></a>
The IAM action to grant or revoke permissions on\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Principal`  <a name="cfn-quicksight-analysis-resourcepermission-principal"></a>
The Amazon Resource Name \(ARN\) of the principal\. This can be one of the following:  
+ The ARN of an Amazon QuickSight user or group associated with a data source or dataset\. \(This is common\.\)
+ The ARN of an Amazon QuickSight user, group, or namespace associated with an analysis, dashboard, template, or theme\. \(This is common\.\)
+ The ARN of an AWS account root: This is an IAM ARN rather than a QuickSight ARN\. Use this option only to share resources \(templates\) across AWS accounts\. \(This is less common\.\)
A *sheet*, which is an object that contains a set of visuals that are viewed together on one page in the Amazon QuickSight console\. Every analysis and dashboard contains at least one sheet\. Each sheet contains at least one visualization widget, for example a chart, pivot table, or narrative insight\. Sheets can be associated with other components, such as controls, filters, and so on\.  
The unique identifier associated with a sheet\.  
The name of a sheet\. This name is displayed on the sheet's tab in the QuickSight console\.  
A string parameter\.  
The values of a string parameter\.  
A display name for a string parameter\.  
Creates a dataset\.  
The time this dataset version was created\.  
The time this dataset version was last updated\.  
  
  
The Amazon Resource Name \(ARN\) of the dataset\.  
Groupings of columns that work together in certain QuickSight features\. Currently, only geospatial hierarchy is supported\.  
Declares the physical tables that are available in the underlying data sources\.  
Indicates whether you want to import the data into SPICE\.  
The folder that contains fields and nested subfolders for your dataset\.  
Configures the combination and transformation of the data from the physical tables\.  
The AWS account ID\.  
A list of resource permissions on the dataset\.  
An ID for the dataset that you want to create\. This ID is unique per AWS Region for each AWS account\.  
The row\-level security configuration for the data that you want to create\.  
Contains a map of the key\-value pairs for the resource tag or tags assigned to the dataset\.  
A set of one or more definitions of a ` ColumnLevelPermissionRule `\.  
The display name for the dataset\.  
A calculated column for a dataset\.  
A unique ID to identify a calculated column\. During a dataset update, if the column ID of a calculated column matches that of an existing calculated column, Amazon QuickSight preserves the existing calculated column\.  
Column name\.  
An expression that defines the calculated column\.  
A transform operation that casts a column to a different type\.  
Column name\.  
When casting a column from string to datetime type, you can supply a string in a format supported by Amazon QuickSight to denote the source data format\.  
New column data type\.  
Metadata that contains a description for a column\.  
The text of a description for a column\.  
Groupings of columns that work together in certain Amazon QuickSight features\. This is a variant type structure\. For this structure to be valid, only one of the attributes can be non\-null\.  
Geospatial column group that denotes a hierarchy\.  
A rule defined to grant access on one or more restricted columns\. Each dataset can have multiple rules\. To create a restricted column, you add it to one or more rules\. Each rule must contain at least one column and at least one user or group\. To be able to see a restricted column, a user or group needs to be added to a rule for that column\.  
An array of column names\.  
An array of Amazon Resource Names \(ARNs\) for QuickSight users or groups\.  
A tag for a column in a [TagColumnOperation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-quicksight-dataset-transformoperation.html#cfn-quicksight-dataset-transformoperation-tagcolumnoperation) structure\. This is a variant type structure\. For this structure to be valid, only one of the attributes can be non\-null\.  
A geospatial role for a column\.  
A description for a column\.  
A transform operation that creates calculated columns\. Columns created in one such operation form a lexical closure\.  
Calculated columns to create\.  
A physical table type built from the results of the custom SQL query\.  
The Amazon Resource Name \(ARN\) of the data source\.  
The SQL query\.  
The column schema from the SQL query result set\.  
A display name for the SQL query result\.  
A FieldFolder element is a folder that contains fields and nested subfolders\.  
The description for a field folder\.  
A folder has a list of columns\. A column can only be in one folder\.  
A transform operation that filters rows based on a condition\.  
An expression that must evaluate to a Boolean value\. Rows for which the expression evaluates to true are kept in the dataset\.  
Geospatial column group that denotes a hierarchy\.  
Columns in this hierarchy\.  
Country code\.  
A display name for the hierarchy\.  
The wait policy to use when creating or updating a Dataset\. The default is to wait for SPICE ingestion to finish with timeout of 36 hours\.  
The wait policy to use when creating or updating a Dataset\. The default is to wait for SPICE ingestion to finish with timeout of 36 hours\.  
Wait for SPICE ingestion to finish to mark dataset creation or update as successful\. Default \(true\)\. Applicable only when `DataSetImportMode` mode is set to SPICE\.  
The maximum time \(in hours\) to wait for Ingestion to complete\. Default timeout is 36 hours\. Applicable only when `DataSetImportMode` mode is set to SPICE and `WaitForSpiceIngestion` is set to true\.  
Metadata for a column that is used as the input of a transform operation\.  
The data type of the column\.  
The name of this column in the underlying data source\.  
The instructions associated with a join\.   
The join instructions provided in the `ON` clause of a join\.  
The type of join that it is\.  
Join key properties of the left operand\.  
The operand on the left side of a join\.  
The operand on the right side of a join\.  
Join key properties of the right operand\.  
Properties associated with the columns participating in a join\.  
A value that indicates that a row in a table is uniquely identified by the columns in a join key\. This is used by QuickSight to optimize query performance\.  
A *logical table* is a unit that joins and that data transformations operate on\. A logical table has a source, which can be either a physical table or result of a join\. When a logical table points to a physical table, the logical table acts as a mutable copy of that physical table through transform operations\.  
A display name for the logical table\.  
Transform operations that act on this logical table\.  
Source of this logical table\.  
Information about the source of a logical table\. This is a variant type structure\. For this structure to be valid, only one of the attributes can be non\-null\.  
Physical table ID\.  
Specifies the result of a join of two logical tables\.  
Output column\.  
Type\.  
A description for a column\.  
A display name for the dataset\.  
A view of a data source that contains information about the shape of the data in the underlying source\. This is a variant type structure\. For this structure to be valid, only one of the attributes can be non\-null\.  
A physical table type for relational data sources\.  
A physical table type built from the results of the custom SQL query\.  
A physical table type for as S3 data source\.  
A transform operation that projects columns\. Operations that come after a projection can only refer to projected columns\.  
Projected columns\.  
A physical table type for relational data sources\.  
The Amazon Resource Name \(ARN\) for the data source\.  
The column schema of the table\.  
The schema name\. This name applies to certain relational database engines\.  
The catalog associated with a table\.  
The name of the relational table\.  
A transform operation that renames a column\.  
The new name for the column\.  
The name of the column to be renamed\.  
Permission for the resource\.  
The IAM action to grand or revoke permisions on  
The Amazon Resource Name \(ARN\) of the principal\. This can be one of the following:  
+ The ARN of an Amazon QuickSight user or group associated with a data source or dataset\. \(This is common\.\)
+ The ARN of an Amazon QuickSight user, group, or namespace associated with an analysis, dashboard, template, or theme\. \(This is common\.\)
+ The ARN of an AWS account root: This is an IAM ARN rather than a QuickSight ARN\. Use this option only to share resources \(templates\) across AWS accounts\. \(This is less common\.\)
Information about a dataset that contains permissions for row\-level security \(RLS\)\. The permissions dataset maps fields to users or groups\. For more information, see [Using Row\-Level Security \(RLS\) to Restrict Access to a Dataset](https://docs.aws.amazon.com/quicksight/latest/user/restrict-access-to-a-data-set-using-row-level-security.html) in the *Amazon QuickSight User Guide*\.  
The option to deny permissions by setting `PermissionPolicy` to `DENY_ACCESS` is not supported for new RLS datasets\.  
The Amazon Resource Name \(ARN\) of the dataset that contains permissions for RLS\.  
The namespace associated with the dataset that contains permissions for RLS\.  
The type of permissions to use when interpretting the permissions for RLS\. `DENY_ACCESS` is included for backward compatibility only\.  
A physical table type for as S3 data source\.  
The Amazon Resource Name \(ARN\) for the data source\.  
A physical table type for as S3 data source\.  
Information about the format for the S3 source file or files\.  
A transform operation that tags a column with additional information\.  
The column that this operation acts on\.  
The dataset column tag, currently only used for geospatial type tagging\.  
This is not tags for the AWS tagging feature\.
A data transformation on a logical table\. This is a variant type structure\. For this structure to be valid, only one of the attributes can be non\-null\.  
An operation that tags a column with additional information\.  
An operation that filters rows based on some condition\.  
A transform operation that casts a column to a different type\.  
An operation that creates calculated columns\. Columns created in one such operation form a lexical closure\.  
An operation that renames a column\.  
An operation that projects columns\. Operations that come after a projection can only refer to projected columns\.  
Information about the format for a source file or files\.  
Whether the file has a header row, or the files each have a header row\.  
Text qualifier\.  
File format\.  
A row number to start reading data from\.  
The delimiter between values in the file\.  
Creates a data source\.  
The HTTP status of the request\.  
The time that this data source was created\.  
The last time that this data source was updated\.  
The structure of a data source\.  
The Amazon Resource Name \(ARN\) of the dataset\.  
The parameters that QuickSight uses to connect to your underlying source\.  
The type of the data source\. Currently, the supported types for this operation are: `ATHENA, AURORA, AURORA_POSTGRESQL, AMAZON_ELASTICSEARCH, MARIADB, MYSQL, POSTGRESQL, PRESTO, REDSHIFT, S3, SNOWFLAKE, SPARK, SQLSERVER, TERADATA`\. Use `ListDataSources` to return a list of all data sources\.  
 `AMAZON_ELASTICSEARCH` is for Amazon managed Elasticsearch Service\.  
Use this parameter only when you want QuickSight to use a VPC connection when connecting to your underlying source\.  
A set of alternate data source parameters that you want to share for the credentials stored with this data source\. The credentials are applied in tandem with the data source parameters when you copy a data source by using a create or update request\. The API operation compares the `DataSourceParameters` structure that's in the request with the structures in the `AlternateDataSourceParameters` allow list\. If the structures are an exact match, the request is allowed to use the credentials from this existing data source\. If the `AlternateDataSourceParameters` list is null, the `Credentials` originally used with this `DataSourceParameters` are automatically allowed\.  
Error information from the last update or the creation of the data source\.  
The AWS account ID\.  
A list of resource permissions on the data source\.  
Secure Socket Layer \(SSL\) properties that apply when QuickSight connects to your underlying source\.  
The credentials QuickSight that uses to connect to your underlying source\. Currently, only credentials based on user name and password are supported\.  
An ID for the data source\. This ID is unique per AWS Region for each AWS account\.   
Contains a map of the key\-value pairs for the resource tag or tags assigned to the data source\.  
A display name for the data source\.  
Amazon Elasticsearch Service parameters\.  
The Amazon Elasticsearch Service domain\.  
Amazon Athena parameters\.  
The workgroup that Amazon Athena uses\.  
Amazon Aurora parameters\.  
Port\.  
Database\.  
Host\.  
Amazon Aurora with PostgreSQL compatibility parameters\.  
Port\.  
Database\.  
Host\.  
AWS IoT Analytics parameters\.  
Dataset name\.  
The combination of user name and password that are used as credentials\.  
A set of alternate data source parameters that you want to share for these credentials\. The credentials are applied in tandem with the data source parameters when you copy a data source by using a create or update request\. The API operation compares the `DataSourceParameters` structure that's in the request with the structures in the `AlternateDataSourceParameters` allow list\. If the structures are an exact match, the request is allowed to use the new data source with the existing credentials\. If the `AlternateDataSourceParameters` list is null, the `DataSourceParameters` originally used with these `Credentials` is automatically allowed\.  
User name\.  
Password\.  
Data source credentials\. This is a variant type structure\. For this structure to be valid, only one of the attributes can be non\-null\.  
The Amazon Resource Name \(ARN\) of a data source that has the credential pair that you want to use\. When `CopySourceArn` is not null, the credential pair from the data source in the ARN is used as the credentials for the `DataSourceCredentials` structure\.  
Credential pair\. For more information, see [CredentialPair](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-quicksight-datasource-datasourcecredentials.html#cfn-quicksight-datasource-datasourcecredentials-credentialpair)\.  
Error information for the data source creation or update\.  
Error type\.  
Error message\.  
The parameters that Amazon QuickSight uses to connect to your underlying source\. This is a variant type structure\. For this structure to be valid, only one of the attributes can be non\-null\.  
Jira parameters\.  
The base URL of the Jira site\.  
Twitter parameters\.  
Aurora PostgreSQL parameters\.  
ServiceNow parameters\.  
Teradata parameters\.  
Amazon RDS parameters\.  
Amazon Athena parameters\.  
Spark parameters\.  
MariaDB parameters\.  
Presto parameters\.  
AWS IoT Analytics parameters\.  
Amazon Redshift parameters\.  
MySQL parameters\.  
SQL Server parameters\.  
Snowflake parameters\.  
Amazon Elasticsearch Service parameters\.  
PostgreSQL parameters\.  
S3 parameters\.  
Amazon Aurora MySQL parameters\.  
Jira parameters\.  
Amazon S3 manifest file location\.  
Amazon S3 bucket\.  
Amazon S3 key that identifies an object\.  
MariaDB parameters\.  
Port\.  
Database\.  
Host\.  
MySQL parameters\.  
Port\.  
Database\.  
Host\.  
Oracle parameters\.  
Port\.  
Database\.  
Host\.  
Oracle parameters\.  
PostgreSQL parameters\.  
Port\.  
Database\.  
Host\.  
Presto parameters\.  
Port\.  
Host\.  
Catalog\.  
Amazon RDS parameters\.  
Instance ID\.  
Database\.  
Amazon Redshift parameters\. The `ClusterId` field can be blank if `Host` and `Port` are both set\. The `Host` and `Port` fields can be blank if the `ClusterId` field is set\.  
Cluster ID\. This field can be blank if the `Host` and `Port` are provided\.  
Port\. This field can be blank if the `ClusterId` is provided\.  
Database\.  
Host\. This field can be blank if `ClusterId` is provided\.  
Permission for the resource\.  
The IAM action to grant or revoke permissions on\.  
The Amazon Resource Name \(ARN\) of the principal\. This can be one of the following:  
+ The ARN of an Amazon QuickSight user or group associated with a data source or dataset\. \(This is common\.\)
+ The ARN of an Amazon QuickSight user, group, or namespace associated with an analysis, dashboard, template, or theme\. \(This is common\.\)
+ The ARN of an AWS account root: This is an IAM ARN rather than a QuickSight ARN\. Use this option only to share resources \(templates\) across AWS accounts\. \(This is less common\.\)
S3 parameters\.  
Location of the Amazon S3 manifest file\. This is NULL if the manifest file was uploaded in the console\.  
Snowflake parameters\.  
Warehouse\.  
Database\.  
Host\.  
Spark parameters\.  
Port\.  
Host\.  
SQL Server parameters\.  
Port\.  
Database\.  
Host\.  
Secure Socket Layer \(SSL\) properties that apply when QuickSight connects to your underlying data source\.  
A Boolean option to control whether SSL should be disabled\.  
Teradata parameters\.  
Port\.  
Database\.  
Host\.  
VPC connection properties\.  
The Amazon Resource Name \(ARN\) for the VPC connection\.  
Twitter parameters\.  
Twitter query string\.  
Maximum number of rows to query Twitter\.  
ServiceNow parameters\.  
URL of the base site\.  
The structure of a data source\.  
The parameters that Amazon QuickSight uses to connect to your underlying data source\. This is a variant type structure\. For this structure to be valid, only one of the attributes can be non\-null\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)