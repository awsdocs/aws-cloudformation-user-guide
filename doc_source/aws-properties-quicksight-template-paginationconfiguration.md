# AWS::QuickSight::Template PaginationConfiguration<a name="aws-properties-quicksight-template-paginationconfiguration"></a>

The pagination configuration for a table visual or boxplot\.

## Syntax<a name="aws-properties-quicksight-template-paginationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-paginationconfiguration-syntax.json"></a>

```
{
  "[PageNumber](#cfn-quicksight-template-paginationconfiguration-pagenumber)" : Double,
  "[PageSize](#cfn-quicksight-template-paginationconfiguration-pagesize)" : Double
}
```

### YAML<a name="aws-properties-quicksight-template-paginationconfiguration-syntax.yaml"></a>

```
  [PageNumber](#cfn-quicksight-template-paginationconfiguration-pagenumber): Double
  [PageSize](#cfn-quicksight-template-paginationconfiguration-pagesize): Double
```

## Properties<a name="aws-properties-quicksight-template-paginationconfiguration-properties"></a>

`PageNumber`  <a name="cfn-quicksight-template-paginationconfiguration-pagenumber"></a>
Indicates the page number\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PageSize`  <a name="cfn-quicksight-template-paginationconfiguration-pagesize"></a>
Indicates how many items render in one page\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)