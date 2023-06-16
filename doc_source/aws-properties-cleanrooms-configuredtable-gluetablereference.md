# AWS::CleanRooms::ConfiguredTable GlueTableReference<a name="aws-properties-cleanrooms-configuredtable-gluetablereference"></a>

A reference to a table within an AWS Glue data catalog\.

## Syntax<a name="aws-properties-cleanrooms-configuredtable-gluetablereference-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cleanrooms-configuredtable-gluetablereference-syntax.json"></a>

```
{
  "[DatabaseName](#cfn-cleanrooms-configuredtable-gluetablereference-databasename)" : String,
  "[TableName](#cfn-cleanrooms-configuredtable-gluetablereference-tablename)" : String
}
```

### YAML<a name="aws-properties-cleanrooms-configuredtable-gluetablereference-syntax.yaml"></a>

```
  [DatabaseName](#cfn-cleanrooms-configuredtable-gluetablereference-databasename): String
  [TableName](#cfn-cleanrooms-configuredtable-gluetablereference-tablename): String
```

## Properties<a name="aws-properties-cleanrooms-configuredtable-gluetablereference-properties"></a>

`DatabaseName`  <a name="cfn-cleanrooms-configuredtable-gluetablereference-databasename"></a>
The name of the database the AWS Glue table belongs to\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9_](([a-zA-Z0-9_ ]+-)*([a-zA-Z0-9_ ]+))?`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TableName`  <a name="cfn-cleanrooms-configuredtable-gluetablereference-tablename"></a>
The name of the AWS Glue table\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9_](([a-zA-Z0-9_ ]+-)*([a-zA-Z0-9_ ]+))?`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)