# AWS::Kendra::DataSource DataSourceToIndexFieldMapping<a name="aws-properties-kendra-datasource-datasourcetoindexfieldmapping"></a>

Maps a column or attribute in the data source to an index field\. You must first create the fields in the index using the [UpdateIndex](https://docs.aws.amazon.com/kendra/latest/dg/API_UpdateIndex.html) operation\.

## Syntax<a name="aws-properties-kendra-datasource-datasourcetoindexfieldmapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-datasourcetoindexfieldmapping-syntax.json"></a>

```
{
  "[DataSourceFieldName](#cfn-kendra-datasource-datasourcetoindexfieldmapping-datasourcefieldname)" : String,
  "[DateFieldFormat](#cfn-kendra-datasource-datasourcetoindexfieldmapping-datefieldformat)" : String,
  "[IndexFieldName](#cfn-kendra-datasource-datasourcetoindexfieldmapping-indexfieldname)" : String
}
```

### YAML<a name="aws-properties-kendra-datasource-datasourcetoindexfieldmapping-syntax.yaml"></a>

```
  [DataSourceFieldName](#cfn-kendra-datasource-datasourcetoindexfieldmapping-datasourcefieldname): String
  [DateFieldFormat](#cfn-kendra-datasource-datasourcetoindexfieldmapping-datefieldformat): String
  [IndexFieldName](#cfn-kendra-datasource-datasourcetoindexfieldmapping-indexfieldname): String
```

## Properties<a name="aws-properties-kendra-datasource-datasourcetoindexfieldmapping-properties"></a>

`DataSourceFieldName`  <a name="cfn-kendra-datasource-datasourcetoindexfieldmapping-datasourcefieldname"></a>
The name of the column or attribute in the data source\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9_.]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DateFieldFormat`  <a name="cfn-kendra-datasource-datasourcetoindexfieldmapping-datefieldformat"></a>
The type of data stored in the column or attribute\.  
*Required*: No  
*Type*: String  
*Minimum*: `4`  
*Maximum*: `40`  
*Pattern*: `^(?!\s).*(?<!\s)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IndexFieldName`  <a name="cfn-kendra-datasource-datasourcetoindexfieldmapping-indexfieldname"></a>
The name of the field in the index\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `30`  
*Pattern*: `^\P{C}*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)