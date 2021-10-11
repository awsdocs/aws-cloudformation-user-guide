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
      "[RetentionProperties](#cfn-timestream-table-retentionproperties)" : Json,
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
  [RetentionProperties](#cfn-timestream-table-retentionproperties): Json
  [TableName](#cfn-timestream-table-tablename): String
  [Tags](#cfn-timestream-table-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-timestream-table-properties"></a>

`DatabaseName`  <a name="cfn-timestream-table-databasename"></a>
The name of the Timestream database that contains this table\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `64`  
*Pattern*: `[a-zA-Z0-9_.-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RetentionProperties`  <a name="cfn-timestream-table-retentionproperties"></a>
The retention duration for the memory store and magnetic store\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableName`  <a name="cfn-timestream-table-tablename"></a>
The name of the Timestream table\.  
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `64`  
*Pattern*: `[a-zA-Z0-9_.-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-timestream-table-tags"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-timestream-table-return-values"></a>

### Ref<a name="aws-resource-timestream-table-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-timestream-table-return-values-fn--getatt"></a>

The `Fn::GetAtt` returns a value for the specified attribute of this type\. The following are the available attributes:

#### <a name="aws-resource-timestream-table-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The `arn` of the table\.

`Name`  <a name="Name-fn::getatt"></a>
The name of the table\.