# AWS::Kendra::DataSource ChangeDetectingColumns<a name="aws-properties-kendra-datasource-changedetectingcolumns"></a>

Columns that indicate when a document in the database has changed\.

## Syntax<a name="aws-properties-kendra-datasource-changedetectingcolumns-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-changedetectingcolumns-syntax.json"></a>

```
{
  "[ChangeDetectingColumns](#cfn-kendra-datasource-changedetectingcolumns-changedetectingcolumns)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-kendra-datasource-changedetectingcolumns-syntax.yaml"></a>

```
  [ChangeDetectingColumns](#cfn-kendra-datasource-changedetectingcolumns-changedetectingcolumns): 
    - String
```

## Properties<a name="aws-properties-kendra-datasource-changedetectingcolumns-properties"></a>

`ChangeDetectingColumns`  <a name="cfn-kendra-datasource-changedetectingcolumns-changedetectingcolumns"></a>
A list of 1 to 5 columns that indicate when a document in the database has changed\.  
*Required*: No  
*Type*: [List](#aws-properties-kendra-datasource-changedetectingcolumns) of [String](#aws-properties-kendra-datasource-changedetectingcolumns)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)