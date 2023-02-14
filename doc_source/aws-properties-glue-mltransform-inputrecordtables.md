# AWS::Glue::MLTransform InputRecordTables<a name="aws-properties-glue-mltransform-inputrecordtables"></a>

A list of AWS Glue table definitions used by the transform\.

## Syntax<a name="aws-properties-glue-mltransform-inputrecordtables-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-mltransform-inputrecordtables-syntax.json"></a>

```
{
  "[GlueTables](#cfn-glue-mltransform-inputrecordtables-gluetables)" : [ GlueTables, ... ]
}
```

### YAML<a name="aws-properties-glue-mltransform-inputrecordtables-syntax.yaml"></a>

```
  [GlueTables](#cfn-glue-mltransform-inputrecordtables-gluetables): 
    - GlueTables
```

## Properties<a name="aws-properties-glue-mltransform-inputrecordtables-properties"></a>

`GlueTables`  <a name="cfn-glue-mltransform-inputrecordtables-gluetables"></a>
The database and table in the AWS Glue Data Catalog that is used for input or output data\.  
*Required*: No  
*Type*: [List](aws-properties-glue-mltransform-inputrecordtables-gluetables.md) of [GlueTables](aws-properties-glue-mltransform-inputrecordtables-gluetables.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)