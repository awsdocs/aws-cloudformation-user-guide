# AWS::Glue::MLTransform GlueTables<a name="aws-properties-glue-mltransform-inputrecordtables-gluetables"></a>

The database and table in the AWS Glue Data Catalog that is used for input or output data\.

## Syntax<a name="aws-properties-glue-mltransform-inputrecordtables-gluetables-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-mltransform-inputrecordtables-gluetables-syntax.json"></a>

```
{
  "[CatalogId](#cfn-glue-mltransform-inputrecordtables-gluetables-catalogid)" : String,
  "[ConnectionName](#cfn-glue-mltransform-inputrecordtables-gluetables-connectionname)" : String,
  "[DatabaseName](#cfn-glue-mltransform-inputrecordtables-gluetables-databasename)" : String,
  "[TableName](#cfn-glue-mltransform-inputrecordtables-gluetables-tablename)" : String
}
```

### YAML<a name="aws-properties-glue-mltransform-inputrecordtables-gluetables-syntax.yaml"></a>

```
  [CatalogId](#cfn-glue-mltransform-inputrecordtables-gluetables-catalogid): String
  [ConnectionName](#cfn-glue-mltransform-inputrecordtables-gluetables-connectionname): String
  [DatabaseName](#cfn-glue-mltransform-inputrecordtables-gluetables-databasename): String
  [TableName](#cfn-glue-mltransform-inputrecordtables-gluetables-tablename): String
```

## Properties<a name="aws-properties-glue-mltransform-inputrecordtables-gluetables-properties"></a>

`CatalogId`  <a name="cfn-glue-mltransform-inputrecordtables-gluetables-catalogid"></a>
A unique identifier for the AWS Glue Data Catalog\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectionName`  <a name="cfn-glue-mltransform-inputrecordtables-gluetables-connectionname"></a>
The name of the connection to the AWS Glue Data Catalog\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseName`  <a name="cfn-glue-mltransform-inputrecordtables-gluetables-databasename"></a>
A database name in the AWS Glue Data Catalog\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableName`  <a name="cfn-glue-mltransform-inputrecordtables-gluetables-tablename"></a>
A table name in the AWS Glue Data Catalog\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)