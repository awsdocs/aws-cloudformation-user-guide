# AWS::CleanRooms::ConfiguredTable<a name="aws-resource-cleanrooms-configuredtable"></a>

Creates a new configured table resource\.

## Syntax<a name="aws-resource-cleanrooms-configuredtable-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cleanrooms-configuredtable-syntax.json"></a>

```
{
  "Type" : "AWS::CleanRooms::ConfiguredTable",
  "Properties" : {
      "[AllowedColumns](#cfn-cleanrooms-configuredtable-allowedcolumns)" : [ String, ... ],
      "[AnalysisMethod](#cfn-cleanrooms-configuredtable-analysismethod)" : String,
      "[AnalysisRules](#cfn-cleanrooms-configuredtable-analysisrules)" : [ AnalysisRule, ... ],
      "[Description](#cfn-cleanrooms-configuredtable-description)" : String,
      "[Name](#cfn-cleanrooms-configuredtable-name)" : String,
      "[TableReference](#cfn-cleanrooms-configuredtable-tablereference)" : TableReference,
      "[Tags](#cfn-cleanrooms-configuredtable-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-cleanrooms-configuredtable-syntax.yaml"></a>

```
Type: AWS::CleanRooms::ConfiguredTable
Properties: 
  [AllowedColumns](#cfn-cleanrooms-configuredtable-allowedcolumns): 
    - String
  [AnalysisMethod](#cfn-cleanrooms-configuredtable-analysismethod): String
  [AnalysisRules](#cfn-cleanrooms-configuredtable-analysisrules): 
    - AnalysisRule
  [Description](#cfn-cleanrooms-configuredtable-description): String
  [Name](#cfn-cleanrooms-configuredtable-name): String
  [TableReference](#cfn-cleanrooms-configuredtable-tablereference): 
    TableReference
  [Tags](#cfn-cleanrooms-configuredtable-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-cleanrooms-configuredtable-properties"></a>

`AllowedColumns`  <a name="cfn-cleanrooms-configuredtable-allowedcolumns"></a>
The columns within the underlying AWS Glue table that can be utilized within collaborations\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AnalysisMethod`  <a name="cfn-cleanrooms-configuredtable-analysismethod"></a>
The analysis method for the configured table\. The only valid value is currently `DIRECT\_QUERY`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DIRECT_QUERY`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AnalysisRules`  <a name="cfn-cleanrooms-configuredtable-analysisrules"></a>
The entire created analysis rule\.  
*Required*: No  
*Type*: List of [AnalysisRule](aws-properties-cleanrooms-configuredtable-analysisrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-cleanrooms-configuredtable-description"></a>
A description for the configured table\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDBFF-\uDC00\uDFFF\t\r\n]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-cleanrooms-configuredtable-name"></a>
A name for the configured table\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `(?!\s*$)[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDBFF-\uDC00\uDFFF\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableReference`  <a name="cfn-cleanrooms-configuredtable-tablereference"></a>
The AWS Glue table that this configured table represents\.  
*Required*: Yes  
*Type*: [TableReference](aws-properties-cleanrooms-configuredtable-tablereference.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-cleanrooms-configuredtable-tags"></a>
An optional label that you can assign to a resource when you create it\. Each tag consists of a key and an optional value, both of which you define\. When you use tagging, you can also use tag\-based access control in IAM policies to control access to this resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cleanrooms-configuredtable-return-values"></a>

### Ref<a name="aws-resource-cleanrooms-configuredtable-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the resource name\. For example: 

`{"Ref": "MyConfiguredTable"}`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cleanrooms-configuredtable-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cleanrooms-configuredtable-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) of the specified configured table\.  
Example: `arn:aws:cleanrooms:us-east-1:111122223333:configuredtable/a1b2c3d4-5678-90ab-cdef-EXAMPLE11111`

`ConfiguredTableIdentifier`  <a name="ConfiguredTableIdentifier-fn::getatt"></a>
Returns the unique identifier of the specified configured table\.  
Example: `a1b2c3d4-5678-90ab-cdef-EXAMPLE33333`

## Examples<a name="aws-resource-cleanrooms-configuredtable--examples"></a>



### A configured table using a list analysis rule<a name="aws-resource-cleanrooms-configuredtable--examples--A_configured_table_using_a_list_analysis_rule_"></a>

The following is an example of a configured table with a list analysis rule applied\.

#### JSON<a name="aws-resource-cleanrooms-configuredtable--examples--A_configured_table_using_a_list_analysis_rule_--json"></a>

```
"ListConfiguredTable": {
  {
    "Type" : "AWS::CleanRooms::ConfiguredTable",
    "Properties" : {
        "Name" : "List Table",
        "Description" : "Example configured table with list AR",
        "AllowedColumns" : ["column1", "column2", "column4"],
        "AnalysisMethod" : "DIRECT_QUERY",
        "AnalysisRules" : [
          "Type": "LIST",
          "Policy": {
            "V1": {
              "List": {
                "JoinColumns": [
                  "column1"
                ],
                "ListColumns": [
                  "column2"
                ]
              }
            }
          }
        ],
        "TableReference" : {
          "Glue": {
            "DatabaseName": "ExampleDB",
            "TableName": "ExampleTable"
          }
        }
      }
  }
}
```

#### YAML<a name="aws-resource-cleanrooms-configuredtable--examples--A_configured_table_using_a_list_analysis_rule_--yaml"></a>

```
ListConfiguredTable:
  Type: AWS::CleanRooms::ConfiguredTable
  Properties:
    Name: List Table
    Description: Example configured table with list AR
    AllowedColumns:
      - column1
      - column2
      - column4
    AnalysisMethod: DIRECT_QUERY
    AnalysisRules:
      - Type: LIST
        Policy:
          V1:
            List:
              JoinColumns:
                - column1
              ListColumns:
                - column2
    TableReference:
      Glue:
        DatabaseName: ExampleDB
        TableName: ExampleTable
```