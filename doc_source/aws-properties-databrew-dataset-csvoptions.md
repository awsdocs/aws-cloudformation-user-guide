# AWS::DataBrew::Dataset CsvOptions<a name="aws-properties-databrew-dataset-csvoptions"></a>

Represents a set of options that define how DataBrew will read a comma\-separated value \(CSV\) file when creating a dataset from that file\.

## Syntax<a name="aws-properties-databrew-dataset-csvoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-dataset-csvoptions-syntax.json"></a>

```
{
  "[Delimiter](#cfn-databrew-dataset-csvoptions-delimiter)" : String,
  "[HeaderRow](#cfn-databrew-dataset-csvoptions-headerrow)" : Boolean
}
```

### YAML<a name="aws-properties-databrew-dataset-csvoptions-syntax.yaml"></a>

```
  [Delimiter](#cfn-databrew-dataset-csvoptions-delimiter): String
  [HeaderRow](#cfn-databrew-dataset-csvoptions-headerrow): Boolean
```

## Properties<a name="aws-properties-databrew-dataset-csvoptions-properties"></a>

`Delimiter`  <a name="cfn-databrew-dataset-csvoptions-delimiter"></a>
A single character that specifies the delimiter being used in the CSV file\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HeaderRow`  <a name="cfn-databrew-dataset-csvoptions-headerrow"></a>
A variable that specifies whether the first row in the file is parsed as the header\. If this value is false, column names are auto\-generated\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)