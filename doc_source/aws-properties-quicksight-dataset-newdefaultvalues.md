# AWS::QuickSight::DataSet NewDefaultValues<a name="aws-properties-quicksight-dataset-newdefaultvalues"></a>

The new default values for the parameter\.

## Syntax<a name="aws-properties-quicksight-dataset-newdefaultvalues-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dataset-newdefaultvalues-syntax.json"></a>

```
{
  "[DateTimeStaticValues](#cfn-quicksight-dataset-newdefaultvalues-datetimestaticvalues)" : [ String, ... ],
  "[DecimalStaticValues](#cfn-quicksight-dataset-newdefaultvalues-decimalstaticvalues)" : [ Double, ... ],
  "[IntegerStaticValues](#cfn-quicksight-dataset-newdefaultvalues-integerstaticvalues)" : [ Double, ... ],
  "[StringStaticValues](#cfn-quicksight-dataset-newdefaultvalues-stringstaticvalues)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dataset-newdefaultvalues-syntax.yaml"></a>

```
  [DateTimeStaticValues](#cfn-quicksight-dataset-newdefaultvalues-datetimestaticvalues): 
    - String
  [DecimalStaticValues](#cfn-quicksight-dataset-newdefaultvalues-decimalstaticvalues): 
    - Double
  [IntegerStaticValues](#cfn-quicksight-dataset-newdefaultvalues-integerstaticvalues): 
    - Double
  [StringStaticValues](#cfn-quicksight-dataset-newdefaultvalues-stringstaticvalues): 
    - String
```

## Properties<a name="aws-properties-quicksight-dataset-newdefaultvalues-properties"></a>

`DateTimeStaticValues`  <a name="cfn-quicksight-dataset-newdefaultvalues-datetimestaticvalues"></a>
A list of static default values for a given date time parameter\. The valid format for this property is `yyyy-MM-dd’T’HH:mm:ss’Z’`\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `32`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DecimalStaticValues`  <a name="cfn-quicksight-dataset-newdefaultvalues-decimalstaticvalues"></a>
A list of static default values for a given decimal parameter\.  
*Required*: No  
*Type*: List of Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntegerStaticValues`  <a name="cfn-quicksight-dataset-newdefaultvalues-integerstaticvalues"></a>
A list of static default values for a given integer parameter\.  
*Required*: No  
*Type*: List of Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StringStaticValues`  <a name="cfn-quicksight-dataset-newdefaultvalues-stringstaticvalues"></a>
A list of static default values for a given string parameter\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)