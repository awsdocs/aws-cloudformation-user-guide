# AWS::LakeFormation::DataCellsFilter<a name="aws-resource-lakeformation-datacellsfilter"></a>

A structure that represents a data cell filter with column\-level, row\-level, and/or cell\-level security\. Data cell filters belong to a specific table in a Data Catalog\. During a stack operation, AWS CloudFormation calls the AWS Lake Formation `CreateDataCellsFilter` API operation to create a `DataCellsFilter` resource, and calls the `DeleteDataCellsFilter` API operation to delete it\. 

## Syntax<a name="aws-resource-lakeformation-datacellsfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lakeformation-datacellsfilter-syntax.json"></a>

```
{
  "Type" : "AWS::LakeFormation::DataCellsFilter",
  "Properties" : {
      "[ColumnNames](#cfn-lakeformation-datacellsfilter-columnnames)" : [ String, ... ],
      "[ColumnWildcard](#cfn-lakeformation-datacellsfilter-columnwildcard)" : ColumnWildcard,
      "[DatabaseName](#cfn-lakeformation-datacellsfilter-databasename)" : String,
      "[Name](#cfn-lakeformation-datacellsfilter-name)" : String,
      "[RowFilter](#cfn-lakeformation-datacellsfilter-rowfilter)" : RowFilter,
      "[TableCatalogId](#cfn-lakeformation-datacellsfilter-tablecatalogid)" : String,
      "[TableName](#cfn-lakeformation-datacellsfilter-tablename)" : String
    }
}
```

### YAML<a name="aws-resource-lakeformation-datacellsfilter-syntax.yaml"></a>

```
Type: AWS::LakeFormation::DataCellsFilter
Properties: 
  [ColumnNames](#cfn-lakeformation-datacellsfilter-columnnames): 
    - String
  [ColumnWildcard](#cfn-lakeformation-datacellsfilter-columnwildcard): 
    ColumnWildcard
  [DatabaseName](#cfn-lakeformation-datacellsfilter-databasename): String
  [Name](#cfn-lakeformation-datacellsfilter-name): String
  [RowFilter](#cfn-lakeformation-datacellsfilter-rowfilter): 
    RowFilter
  [TableCatalogId](#cfn-lakeformation-datacellsfilter-tablecatalogid): String
  [TableName](#cfn-lakeformation-datacellsfilter-tablename): String
```

## Properties<a name="aws-resource-lakeformation-datacellsfilter-properties"></a>

`ColumnNames`  <a name="cfn-lakeformation-datacellsfilter-columnnames"></a>
An array of UTF\-8 strings\. A list of column names\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ColumnWildcard`  <a name="cfn-lakeformation-datacellsfilter-columnwildcard"></a>
A wildcard with exclusions\. You must specify either a `ColumnNames` list or the `ColumnWildCard`\.   
*Required*: No  
*Type*: [ColumnWildcard](aws-properties-lakeformation-datacellsfilter-columnwildcard.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DatabaseName`  <a name="cfn-lakeformation-datacellsfilter-databasename"></a>
UTF\-8 string, not less than 1 or more than 255 bytes long, matching the [single\-line string pattern](lake-formation/latest/dg/aws-lake-formation-api-aws-lake-formation-api-common.html#aws-glue-api-regex-oneLine)\.  
A database in the Data Catalog\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-lakeformation-datacellsfilter-name"></a>
UTF\-8 string, not less than 1 or more than 255 bytes long, matching the [single\-line string pattern](lake-formation/latest/dg/aws-lake-formation-api-aws-lake-formation-api-common.html#aws-glue-api-regex-oneLine)\.  
The name given by the user to the data filter cell\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RowFilter`  <a name="cfn-lakeformation-datacellsfilter-rowfilter"></a>
 A PartiQL predicate\.   
*Required*: No  
*Type*: [RowFilter](aws-properties-lakeformation-datacellsfilter-rowfilter.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TableCatalogId`  <a name="cfn-lakeformation-datacellsfilter-tablecatalogid"></a>
Catalog id string, not less than 1 or more than 255 bytes long, matching the [single\-line string pattern](lake-formation/latest/dg/aws-lake-formation-api-aws-lake-formation-api-common.html#aws-glue-api-regex-oneLine)\.  
The ID of the catalog to which the table belongs\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TableName`  <a name="cfn-lakeformation-datacellsfilter-tablename"></a>
 UTF\-8 string, not less than 1 or more than 255 bytes long, matching the [single\-line string pattern](lake-formation/latest/dg/aws-lake-formation-api-aws-lake-formation-api-common.html#aws-glue-api-regex-oneLine)\.  
A table in the database\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-lakeformation-datacellsfilter-return-values"></a>

### Ref<a name="aws-resource-lakeformation-datacellsfilter-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource properties such as TableCatalogId, DatabaseName, TableName, and FilterName\. For example: 123456789012\|ExampleDbName\|ExampleTableName\|ExampleFilterName

## Remarks<a name="aws-resource-lakeformation-datacellsfilter--remarks"></a>

The level of filtering that you get depends on how you populate the data filter\.
+ When you specify the "all columns" wildcard and provide a row filter expression, you are establishing row\-level security \(row filtering\) only\.
+ When you include or exclude specific columns and specify *all rows* using the all\-rows wildcard, you are establishing column\-level security \(column filtering\) only\.
+ When you include or exclude specific columns and also provide a row filter expression, you are establishing cell\-level security \(cell filtering\)\.

 *Specify the following to create a valid data cells filter:*
+ `ColumnWildcard` or `ColumnNames`
+ `RowFilter.AllRowsWildcard` or `RowFilter.FilterExpression`

## Examples<a name="aws-resource-lakeformation-datacellsfilter--examples"></a>

### Creating a DataCellsFilter using row and column wildcards<a name="aws-resource-lakeformation-datacellsfilter--examples--Creating_a_DataCellsFilter_using_row_and_column_wildcards"></a>

The following example demonstrates how to create a `DataCellsFilter` resource using row and column wildcards:

#### JSON<a name="aws-resource-lakeformation-datacellsfilter--examples--Creating_a_DataCellsFilter_using_row_and_column_wildcards--json"></a>

```
{
  "SampleDataCellsFilter": {
    "Type": "AWS::LakeFormation::DataCellsFilter",
    "Properties": {
      "TableCatalogId": "12345678910",
      "DatabaseName": "sample_db",
      "TableName": "sample_tbl",
      "Name": "sample_data_cells_filter",
      "RowFilter": {
          "AllRowsWildcard": {}
       },
          "ColumnWildcard": {}
     }
   }
}
```

#### YAML<a name="aws-resource-lakeformation-datacellsfilter--examples--Creating_a_DataCellsFilter_using_row_and_column_wildcards--yaml"></a>

```
SampleDataCellsFilter:
    Type: AWS::LakeFormation::DataCellsFilter
    Properties:
        TableCatalogId: "12345678910"
        DatabaseName: "sample_db" 
        TableName: "sample_tbl" 
        Name: "sample_data_cells_filter" 
        RowFilter: 
            AllRowsWildcard: {}
        ColumnWildcard: {}
```

### Creating a DataCellsFilter using a row wild card and specified columns<a name="aws-resource-lakeformation-datacellsfilter--examples--Creating_a_DataCellsFilter_using_a_row_wild_card_and_specified_columns"></a>

The following example demonstrates how to create a `DataCellsFilter` resource using a row wild card and specified columns:

#### JSON<a name="aws-resource-lakeformation-datacellsfilter--examples--Creating_a_DataCellsFilter_using_a_row_wild_card_and_specified_columns--json"></a>

```
{
    "SampleDataCellsFilter": {
        "Type": "AWS::LakeFormation::DataCellsFilter",
        "Properties": {
            "TableCatalogId": "12345678910",
            "DatabaseName": "sample_db",
            "TableName": "sample_tbl",
            "Name": "sample_data_cells_filter",
            "RowFilter": {
                "AllRowsWildcard": {}
            },
            "ColumnNames": ["sample_column_1", "sample_column_2"]
        }
    }
}
```

#### YAML<a name="aws-resource-lakeformation-datacellsfilter--examples--Creating_a_DataCellsFilter_using_a_row_wild_card_and_specified_columns--yaml"></a>

```
SampleDataCellsFilter:
    Type: AWS::LakeFormation::DataCellsFilter
    Properties:
        TableCatalogId: "12345678910"
        DatabaseName: "sample_db" 
        TableName: "sample_tbl" 
        Name: "sample_data_cells_filter" 
        RowFilter: 
            AllRowsWildcard: {}
        ColumnNames: ["sample_column_1", "sample_column_2"]
```

### Creating a DataCellsFilter using a row filter expression and a column wildcard<a name="aws-resource-lakeformation-datacellsfilter--examples--Creating_a_DataCellsFilter_using_a_row_filter_expression_and_a_column_wildcard"></a>

The following example demonstrates how to create a `DataCellsFilter` using a row filter expression and a column wildcard:

#### JSON<a name="aws-resource-lakeformation-datacellsfilter--examples--Creating_a_DataCellsFilter_using_a_row_filter_expression_and_a_column_wildcard--json"></a>

```
{
    "SampleDataCellsFilter": {
        "Type": "AWS::LakeFormation::DataCellsFilter",
        "Properties": {
            "TableCatalogId": "12345678910",
            "DatabaseName": "sample_db",
            "TableName": "sample_tbl",
            "Name": "sample_data_cells_filter",
            "RowFilter": {
                "FilterExpression": "sample_column_1 > 0"
            },
            "ColumnWildcard": {}
        }
    }
}
```

#### YAML<a name="aws-resource-lakeformation-datacellsfilter--examples--Creating_a_DataCellsFilter_using_a_row_filter_expression_and_a_column_wildcard--yaml"></a>

```
SampleDataCellsFilter:
    Type: AWS::LakeFormation::DataCellsFilter
    Properties:
        TableCatalogId: "12345678910"
        DatabaseName: "sample_db" 
        TableName: "sample_tbl" 
        Name: "sample_data_cells_filter" 
        RowFilter: 
            FilterExpression: "sample_column_1 > 0"
        ColumnWildcard: {}
```

### Creating a DataCellsFilter using a row filter and specified columns<a name="aws-resource-lakeformation-datacellsfilter--examples--Creating_a_DataCellsFilter_using_a_row_filter_and_specified_columns"></a>

The following example demonstrates how to create a `DataCellsFilter` resource using a row filter and specified columns:

#### JSON<a name="aws-resource-lakeformation-datacellsfilter--examples--Creating_a_DataCellsFilter_using_a_row_filter_and_specified_columns--json"></a>

```
{
    "SampleDataCellsFilter": {
        "Type": "AWS::LakeFormation::DataCellsFilter",
        "Properties": {
            "TableCatalogId": "12345678910",
            "DatabaseName": "sample_db",
            "TableName": "sample_tbl",
            "Name": "sample_data_cells_filter",
            "RowFilter": {
                "FilterExpression": "sample_column_1 > 0"
            },
            "ColumnNames": ["sample_column_1", "sample_column_2"]
        }
    }
}
```

#### YAML<a name="aws-resource-lakeformation-datacellsfilter--examples--Creating_a_DataCellsFilter_using_a_row_filter_and_specified_columns--yaml"></a>

```
SampleDataCellsFilter:
    Type: AWS::LakeFormation::DataCellsFilter
    Properties:
        TableCatalogId: "12345678910"
        DatabaseName: "sample_db" 
        TableName: "sample_tbl" 
        Name: "sample_data_cells_filter" 
        RowFilter: 
            FilterExpression: "sample_column_1 > 0"
        ColumnNames: ["sample_column_1", "sample_column_2"]
```

## See also<a name="aws-resource-lakeformation-datacellsfilter--seealso"></a>

 [ Data filtering and cell\-level security in AWS Lake Formation\.](https://docs.aws.amazon.com/lake-formation/latest/dg/data-filters-about.html) 