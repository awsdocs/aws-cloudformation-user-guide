# AWS::Lightsail::Database<a name="aws-resource-lightsail-database"></a>

The `AWS::Lightsail::Database` resource specifies an Amazon Lightsail database\.

## Syntax<a name="aws-resource-lightsail-database-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lightsail-database-syntax.json"></a>

```
{
  "Type" : "AWS::Lightsail::Database",
  "Properties" : {
      "[AvailabilityZone](#cfn-lightsail-database-availabilityzone)" : String,
      "[BackupRetention](#cfn-lightsail-database-backupretention)" : Boolean,
      "[CaCertificateIdentifier](#cfn-lightsail-database-cacertificateidentifier)" : String,
      "[MasterDatabaseName](#cfn-lightsail-database-masterdatabasename)" : String,
      "[MasterUsername](#cfn-lightsail-database-masterusername)" : String,
      "[MasterUserPassword](#cfn-lightsail-database-masteruserpassword)" : String,
      "[PreferredBackupWindow](#cfn-lightsail-database-preferredbackupwindow)" : String,
      "[PreferredMaintenanceWindow](#cfn-lightsail-database-preferredmaintenancewindow)" : String,
      "[PubliclyAccessible](#cfn-lightsail-database-publiclyaccessible)" : Boolean,
      "[RelationalDatabaseBlueprintId](#cfn-lightsail-database-relationaldatabaseblueprintid)" : String,
      "[RelationalDatabaseBundleId](#cfn-lightsail-database-relationaldatabasebundleid)" : String,
      "[RelationalDatabaseName](#cfn-lightsail-database-relationaldatabasename)" : String,
      "[RelationalDatabaseParameters](#cfn-lightsail-database-relationaldatabaseparameters)" : [ RelationalDatabaseParameter, ... ],
      "[RotateMasterUserPassword](#cfn-lightsail-database-rotatemasteruserpassword)" : Boolean,
      "[Tags](#cfn-lightsail-database-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-lightsail-database-syntax.yaml"></a>

```
Type: AWS::Lightsail::Database
Properties: 
  [AvailabilityZone](#cfn-lightsail-database-availabilityzone): String
  [BackupRetention](#cfn-lightsail-database-backupretention): Boolean
  [CaCertificateIdentifier](#cfn-lightsail-database-cacertificateidentifier): String
  [MasterDatabaseName](#cfn-lightsail-database-masterdatabasename): String
  [MasterUsername](#cfn-lightsail-database-masterusername): String
  [MasterUserPassword](#cfn-lightsail-database-masteruserpassword): String
  [PreferredBackupWindow](#cfn-lightsail-database-preferredbackupwindow): String
  [PreferredMaintenanceWindow](#cfn-lightsail-database-preferredmaintenancewindow): String
  [PubliclyAccessible](#cfn-lightsail-database-publiclyaccessible): Boolean
  [RelationalDatabaseBlueprintId](#cfn-lightsail-database-relationaldatabaseblueprintid): String
  [RelationalDatabaseBundleId](#cfn-lightsail-database-relationaldatabasebundleid): String
  [RelationalDatabaseName](#cfn-lightsail-database-relationaldatabasename): String
  [RelationalDatabaseParameters](#cfn-lightsail-database-relationaldatabaseparameters): 
    - RelationalDatabaseParameter
  [RotateMasterUserPassword](#cfn-lightsail-database-rotatemasteruserpassword): Boolean
  [Tags](#cfn-lightsail-database-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-lightsail-database-properties"></a>

`AvailabilityZone`  <a name="cfn-lightsail-database-availabilityzone"></a>
The Availability Zone for the database\.  
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.

`BackupRetention`  <a name="cfn-lightsail-database-backupretention"></a>
A Boolean value indicating whether automated backup retention is enabled for the database\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`CaCertificateIdentifier`  <a name="cfn-lightsail-database-cacertificateidentifier"></a>
The certificate associated with the database\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MasterDatabaseName`  <a name="cfn-lightsail-database-masterdatabasename"></a>
The meaning of this parameter differs according to the database engine you use\.  
 **MySQL**   
The name of the database to create when the Lightsail database resource is created\. If this parameter isn't specified, no database is created in the database resource\.  
Constraints:  
+ Must contain 1\-64 letters or numbers\.
+ Must begin with a letter\. Subsequent characters can be letters, underscores, or numbers \(0\-9\)\.
+ Can't be a word reserved by the specified database engine\.

  For more information about reserved words in MySQL, see the Keywords and Reserved Words articles for [MySQL 5\.6](https://dev.mysql.com/doc/refman/5.6/en/keywords.html), [MySQL 5\.7](https://dev.mysql.com/doc/refman/5.7/en/keywords.html), and [MySQL 8\.0](https://dev.mysql.com/doc/refman/8.0/en/keywords.html)\.
 **PostgreSQL**   
The name of the database to create when the Lightsail database resource is created\. If this parameter isn't specified, a database named `postgres` is created in the database resource\.  
Constraints:  
+ Must contain 1\-63 letters or numbers\.
+ Must begin with a letter\. Subsequent characters can be letters, underscores, or numbers \(0\-9\)\.
+ Can't be a word reserved by the specified database engine\.

  For more information about reserved words in PostgreSQL, see the SQL Key Words articles for [PostgreSQL 9\.6](https://www.postgresql.org/docs/9.6/sql-keywords-appendix.html), [PostgreSQL 10](https://www.postgresql.org/docs/10/sql-keywords-appendix.html), [PostgreSQL 11](https://www.postgresql.org/docs/11/sql-keywords-appendix.html), and [PostgreSQL 12](https://www.postgresql.org/docs/12/sql-keywords-appendix.html)\.
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`MasterUsername`  <a name="cfn-lightsail-database-masterusername"></a>
The name for the primary user\.  
 **MySQL**   
Constraints:  
+ Required for MySQL\.
+ Must be 1\-16 letters or numbers\. Can contain underscores\.
+ First character must be a letter\.
+ Can't be a reserved word for the chosen database engine\.

  For more information about reserved words in MySQL 5\.6 or 5\.7, see the Keywords and Reserved Words articles for [MySQL 5\.6](https://dev.mysql.com/doc/refman/5.6/en/keywords.html), [MySQL 5\.7](https://dev.mysql.com/doc/refman/5.7/en/keywords.html), or [MySQL 8\.0](https://dev.mysql.com/doc/refman/8.0/en/keywords.html)\.
 **PostgreSQL**   
Constraints:  
+ Required for PostgreSQL\.
+ Must be 1\-63 letters or numbers\. Can contain underscores\.
+ First character must be a letter\.
+ Can't be a reserved word for the chosen database engine\.

  For more information about reserved words in MySQL 5\.6 or 5\.7, see the Keywords and Reserved Words articles for [PostgreSQL 9\.6](https://www.postgresql.org/docs/9.6/sql-keywords-appendix.html), [PostgreSQL 10](https://www.postgresql.org/docs/10/sql-keywords-appendix.html), [PostgreSQL 11](https://www.postgresql.org/docs/11/sql-keywords-appendix.html), and [PostgreSQL 12](https://www.postgresql.org/docs/12/sql-keywords-appendix.html)\.
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`MasterUserPassword`  <a name="cfn-lightsail-database-masteruserpassword"></a>
The password for the primary user of the database\. The password can include any printable ASCII character except the following: /, ", or @\. It cannot contain spaces\.  
The `MasterUserPassword` and `RotateMasterUserPassword` parameters cannot be used together in the same template\.
 **MySQL**   
Constraints: Must contain 8\-41 characters\.  
 **PostgreSQL**   
Constraints: Must contain 8\-128 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreferredBackupWindow`  <a name="cfn-lightsail-database-preferredbackupwindow"></a>
The daily time range during which automated backups are created for the database \(for example, `16:00-16:30`\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreferredMaintenanceWindow`  <a name="cfn-lightsail-database-preferredmaintenancewindow"></a>
The weekly time range during which system maintenance can occur for the database, formatted as follows: `ddd:hh24:mi-ddd:hh24:mi`\. For example, `Tue:17:00-Tue:17:30`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PubliclyAccessible`  <a name="cfn-lightsail-database-publiclyaccessible"></a>
A Boolean value indicating whether the database is accessible to anyone on the internet\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RelationalDatabaseBlueprintId`  <a name="cfn-lightsail-database-relationaldatabaseblueprintid"></a>
The blueprint ID for the database \(for example, `mysql_8_0`\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`RelationalDatabaseBundleId`  <a name="cfn-lightsail-database-relationaldatabasebundleid"></a>
The bundle ID for the database \(for example, `medium_1_0`\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: Updates are not supported\.

`RelationalDatabaseName`  <a name="cfn-lightsail-database-relationaldatabasename"></a>
The name of the instance\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RelationalDatabaseParameters`  <a name="cfn-lightsail-database-relationaldatabaseparameters"></a>
An array of parameters for the database\.  
*Required*: No  
*Type*: List of [RelationalDatabaseParameter](aws-properties-lightsail-database-relationaldatabaseparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RotateMasterUserPassword`  <a name="cfn-lightsail-database-rotatemasteruserpassword"></a>
A Boolean value indicating whether to change the primary user password to a new, strong password generated by Lightsail\.  
The `RotateMasterUserPassword` and `MasterUserPassword` parameters cannot be used together in the same template\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-lightsail-database-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html) in the *AWS CloudFormation User Guide*\.  
The `Value` of `Tags` is optional for Lightsail resources\.
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-lightsail-database-return-values"></a>

### Ref<a name="aws-resource-lightsail-database-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a unique identifier for this resource\.

### Fn::GetAtt<a name="aws-resource-lightsail-database-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-lightsail-database-return-values-fn--getatt-fn--getatt"></a>

`DatabaseArn`  <a name="DatabaseArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the database \(for example, `arn:aws:lightsail:us-east-2:123456789101:RelationalDatabase/244ad76f-8aad-4741-809f-12345EXAMPLE`\)\.

## Remarks<a name="aws-resource-lightsail-database--remarks"></a>

*Availability Zone*

You can specify an Availability Zone when you perform a create database request\. If you don’t specify one, the database is created in the same Availability Zone as the last Lightsail resource you created\.

*Database updates*

All database update operations are performed immediately\. However, parameter updates are applied based on the `ApplyMethod` value for the specific parameter being updated\.