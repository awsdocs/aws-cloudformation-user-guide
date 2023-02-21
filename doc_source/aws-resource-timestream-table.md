# AWS::Timestream::Table<a name="aws-resource-timestream-table"></a>

The CreateTable operation adds a new table to an existing database in your account\. In an AWS account, table names must be at least unique within each Region if they are in the same database\. You may have identical table names in the same Region if the tables are in separate databases\. While creating the table, you must specify the table name, database name, and the retention properties\. [Service quotas apply](https://docs.aws.amazon.com/timestream/latest/developerguide/ts-limits.html)\. See [code sample](https://docs.aws.amazon.com/timestream/latest/developerguide/code-samples.create-table.html) for details\. 

## Syntax<a name="aws-resource-timestream-table-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-timestream-table-syntax.json"></a>

```
{
  "Type" : "AWS::Timestream::Table",
  "Properties" : {
      "[DatabaseName](#cfn-timestream-table-databasename)" : String,
      "[MagneticStoreWriteProperties](#cfn-timestream-table-magneticstorewriteproperties)" : MagneticStoreWriteProperties,
      "[RetentionProperties](#cfn-timestream-table-retentionproperties)" : RetentionProperties,
      "[TableName](#cfn-timestream-table-tablename)" : String,
      "[Tags](#cfn-timestream-table-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-timestream-table-syntax.yaml"></a>

```
Type: AWS::Timestream::Table
Properties: 
  [DatabaseName](#cfn-timestream-table-databasename): String
  [MagneticStoreWriteProperties](#cfn-timestream-table-magneticstorewriteproperties): 
    MagneticStoreWriteProperties
  [RetentionProperties](#cfn-timestream-table-retentionproperties): 
    RetentionProperties
  [TableName](#cfn-timestream-table-tablename): String
  [Tags](#cfn-timestream-table-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-timestream-table-properties"></a>

`DatabaseName`  <a name="cfn-timestream-table-databasename"></a>
The name of the Timestream database that contains this table\.  
*Length Constraints*: Minimum length of 3 bytes\. Maximum length of 256 bytes\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MagneticStoreWriteProperties`  <a name="cfn-timestream-table-magneticstorewriteproperties"></a>
Contains properties to set on the table when enabling magnetic store writes\.  
This object has the following attributes:  
+ *EnableMagneticStoreWrites*: A `boolean` flag to enable magnetic store writes\.
+ *MagneticStoreRejectedDataLocation*: The location to write error reports for records rejected, asynchronously, during magnetic store writes\. Only `S3Configuration` objects are allowed\. The `S3Configuration` object has the following attributes: 
  + *BucketName*: The name of the S3 bucket\.
  + *EncryptionOption*: The encryption option for the S3 location\. Valid values are S3 server\-side encryption with an S3 managed key \(`SSE_S3`\) or AWS managed key \(` SSE_KMS`\)\.
  + *KmsKeyId*: The AWS KMS key ID to use when encrypting with an AWS managed key\.
  + *ObjectKeyPrefix*: The prefix to use option for the objects stored in S3\.

  Both `BucketName` and `EncryptionOption` are **required** when `S3Configuration` is specified\. If you specify ` SSE_KMS` as your `EncryptionOption` then `KmsKeyId` is **required**\.
 `EnableMagneticStoreWrites` attribute is **required** when `MagneticStoreWriteProperties` is specified\. `MagneticStoreRejectedDataLocation` attribute is **required** when `EnableMagneticStoreWrites` is set to `true`\.  
See the following examples:  
**JSON**  

```
{
   "Type" : AWS::Timestream::Table", 
   "Properties":{
      "DatabaseName":"TestDatabase",
      "TableName":"TestTable",
      "MagneticStoreWriteProperties":{
         "EnableMagneticStoreWrites":true,
         "MagneticStoreRejectedDataLocation":{
            "S3Configuration":{
               "BucketName":"testbucket",
               "EncryptionOption":"SSE_KMS",
               "KmsKeyId":"1234abcd-12ab-34cd-56ef-1234567890ab",
               "ObjectKeyPrefix":"prefix"
            }
         }
      }
   }
}
```
**YAML**  

```
Type: AWS::Timestream::Table
DependsOn: TestDatabase
Properties:
  TableName: "TestTable"
  DatabaseName: "TestDatabase"
  MagneticStoreWriteProperties:
    EnableMagneticStoreWrites: true
    MagneticStoreRejectedDataLocation:
      S3Configuration:
        BucketName: "testbucket"
        EncryptionOption: "SSE_KMS"
        KmsKeyId: "1234abcd-12ab-34cd-56ef-1234567890ab"
        ObjectKeyPrefix: "prefix"
```
*Required*: No  
*Type*: [MagneticStoreWriteProperties](aws-properties-timestream-table-magneticstorewriteproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetentionProperties`  <a name="cfn-timestream-table-retentionproperties"></a>
The retention duration for the memory store and magnetic store\. This object has the following attributes:  
+ *MemoryStoreRetentionPeriodInHours*: Retention duration for memory store, in hours\.
+ *MagneticStoreRetentionPeriodInDays*: Retention duration for magnetic store, in days\.
Both attributes are of type `string`\. Both attributes are **required** when `RetentionProperties` is specified\.  
See the following examples:  
**JSON**  

```
{
    "Type" : AWS::Timestream::Table", 
    "Properties" : {
        "DatabaseName" : "TestDatabase", 
        "TableName" : "TestTable", 
        "RetentionProperties" : {
            "MemoryStoreRetentionPeriodInHours": "24",
            "MagneticStoreRetentionPeriodInDays": "7"
        }
    } 
}
```
**YAML**  

```
Type: AWS::Timestream::Table
DependsOn: TestDatabase
Properties:
    TableName: "TestTable"
    DatabaseName: "TestDatabase"
    RetentionProperties:
        MemoryStoreRetentionPeriodInHours: "24"
        MagneticStoreRetentionPeriodInDays: "7"
```
*Required*: No  
*Type*: [RetentionProperties](aws-properties-timestream-table-retentionproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableName`  <a name="cfn-timestream-table-tablename"></a>
The name of the Timestream table\.  
*Length Constraints*: Minimum length of 3 bytes\. Maximum length of 256 bytes\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-timestream-table-tags"></a>
The tags to add to the table  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-timestream-table-return-values"></a>

### Ref<a name="aws-resource-timestream-table-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the table name `TABLE_NAME` in the form `DATABASE_NAME|TABLE_NAME`\. `DATABASE_NAME` is the name of the Timestream database that the table is contained in\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-timestream-table-return-values-fn--getatt"></a>

The `Fn::GetAtt` returns a value for the specified attribute of this type\. The following are the available attributes:

#### <a name="aws-resource-timestream-table-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The `arn` of the table\.

`Name`  <a name="Name-fn::getatt"></a>
The name of the table\.