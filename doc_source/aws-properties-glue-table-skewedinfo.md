# AWS::Glue::Table SkewedInfo<a name="aws-properties-glue-table-skewedinfo"></a>

Specifies skewed values in a table\. Skewed values are those that occur with very high frequency\.

## Syntax<a name="aws-properties-glue-table-skewedinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-table-skewedinfo-syntax.json"></a>

```
{
  "[SkewedColumnNames](#cfn-glue-table-skewedinfo-skewedcolumnnames)" : [ String, ... ],
  "[SkewedColumnValueLocationMaps](#cfn-glue-table-skewedinfo-skewedcolumnvaluelocationmaps)" : Json,
  "[SkewedColumnValues](#cfn-glue-table-skewedinfo-skewedcolumnvalues)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-glue-table-skewedinfo-syntax.yaml"></a>

```
  [SkewedColumnNames](#cfn-glue-table-skewedinfo-skewedcolumnnames): 
    - String
  [SkewedColumnValueLocationMaps](#cfn-glue-table-skewedinfo-skewedcolumnvaluelocationmaps): Json
  [SkewedColumnValues](#cfn-glue-table-skewedinfo-skewedcolumnvalues): 
    - String
```

## Properties<a name="aws-properties-glue-table-skewedinfo-properties"></a>

`SkewedColumnNames`  <a name="cfn-glue-table-skewedinfo-skewedcolumnnames"></a>
A list of names of columns that contain skewed values\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SkewedColumnValueLocationMaps`  <a name="cfn-glue-table-skewedinfo-skewedcolumnvaluelocationmaps"></a>
A mapping of skewed values to the columns that contain them\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SkewedColumnValues`  <a name="cfn-glue-table-skewedinfo-skewedcolumnvalues"></a>
A list of values that appear so frequently as to be considered skewed\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `us-east-1`
- `us-east-2`
- `us-west-2`
