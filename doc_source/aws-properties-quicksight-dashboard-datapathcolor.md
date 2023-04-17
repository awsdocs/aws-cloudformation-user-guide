# AWS::QuickSight::Dashboard DataPathColor<a name="aws-properties-quicksight-dashboard-datapathcolor"></a>

The color map that determines the color options for a particular element\.

## Syntax<a name="aws-properties-quicksight-dashboard-datapathcolor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-datapathcolor-syntax.json"></a>

```
{
  "[Color](#cfn-quicksight-dashboard-datapathcolor-color)" : String,
  "[Element](#cfn-quicksight-dashboard-datapathcolor-element)" : DataPathValue,
  "[TimeGranularity](#cfn-quicksight-dashboard-datapathcolor-timegranularity)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-datapathcolor-syntax.yaml"></a>

```
  [Color](#cfn-quicksight-dashboard-datapathcolor-color): String
  [Element](#cfn-quicksight-dashboard-datapathcolor-element): 
    DataPathValue
  [TimeGranularity](#cfn-quicksight-dashboard-datapathcolor-timegranularity): String
```

## Properties<a name="aws-properties-quicksight-dashboard-datapathcolor-properties"></a>

`Color`  <a name="cfn-quicksight-dashboard-datapathcolor-color"></a>
The color that needs to be applied to the element\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^#[A-F0-9]{6}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Element`  <a name="cfn-quicksight-dashboard-datapathcolor-element"></a>
The element that the color needs to be applied to\.  
*Required*: Yes  
*Type*: [DataPathValue](aws-properties-quicksight-dashboard-datapathvalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeGranularity`  <a name="cfn-quicksight-dashboard-datapathcolor-timegranularity"></a>
The time granularity of the field that the color needs to be applied to\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DAY | HOUR | MILLISECOND | MINUTE | MONTH | QUARTER | SECOND | WEEK | YEAR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)