# AWS::QuickSight::Dashboard DataSetReference<a name="aws-properties-quicksight-dashboard-datasetreference"></a>

Dataset reference\.

## Syntax<a name="aws-properties-quicksight-dashboard-datasetreference-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-datasetreference-syntax.json"></a>

```
{
  "[DataSetArn](#cfn-quicksight-dashboard-datasetreference-datasetarn)" : String,
  "[DataSetPlaceholder](#cfn-quicksight-dashboard-datasetreference-datasetplaceholder)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-datasetreference-syntax.yaml"></a>

```
  [DataSetArn](#cfn-quicksight-dashboard-datasetreference-datasetarn): String
  [DataSetPlaceholder](#cfn-quicksight-dashboard-datasetreference-datasetplaceholder): String
```

## Properties<a name="aws-properties-quicksight-dashboard-datasetreference-properties"></a>

`DataSetArn`  <a name="cfn-quicksight-dashboard-datasetreference-datasetarn"></a>
Dataset Amazon Resource Name \(ARN\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataSetPlaceholder`  <a name="cfn-quicksight-dashboard-datasetreference-datasetplaceholder"></a>
Dataset placeholder\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)