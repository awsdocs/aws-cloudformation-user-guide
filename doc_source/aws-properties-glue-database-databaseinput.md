# AWS::Glue::Database DatabaseInput<a name="aws-properties-glue-database-databaseinput"></a>

The structure used to create or update a database\.

## Syntax<a name="aws-properties-glue-database-databaseinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-database-databaseinput-syntax.json"></a>

```
{
  "[Description](#cfn-glue-database-databaseinput-description)" : String,
  "[LocationUri](#cfn-glue-database-databaseinput-locationuri)" : String,
  "[Name](#cfn-glue-database-databaseinput-name)" : String,
  "[Parameters](#cfn-glue-database-databaseinput-parameters)" : Json,
  "[TargetDatabase](#cfn-glue-database-databaseinput-targetdatabase)" : DatabaseIdentifier
}
```

### YAML<a name="aws-properties-glue-database-databaseinput-syntax.yaml"></a>

```
  [Description](#cfn-glue-database-databaseinput-description): String
  [LocationUri](#cfn-glue-database-databaseinput-locationuri): String
  [Name](#cfn-glue-database-databaseinput-name): String
  [Parameters](#cfn-glue-database-databaseinput-parameters): Json
  [TargetDatabase](#cfn-glue-database-databaseinput-targetdatabase): 
    DatabaseIdentifier
```

## Properties<a name="aws-properties-glue-database-databaseinput-properties"></a>

`Description`  <a name="cfn-glue-database-databaseinput-description"></a>
A description of the database\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LocationUri`  <a name="cfn-glue-database-databaseinput-locationuri"></a>
The location of the database \(for example, an HDFS path\)\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-glue-database-databaseinput-name"></a>
The name of the database\. For Hive compatibility, this is folded to lowercase when it is stored\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Parameters`  <a name="cfn-glue-database-databaseinput-parameters"></a>
These key\-value pairs define parameters and properties of the database\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetDatabase`  <a name="cfn-glue-database-databaseinput-targetdatabase"></a>
A `DatabaseIdentifier` structure that describes a target database for resource linking\.  
*Required*: No  
*Type*: [DatabaseIdentifier](aws-properties-glue-database-databaseidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)