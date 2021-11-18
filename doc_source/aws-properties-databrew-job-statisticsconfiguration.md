# AWS::DataBrew::Job StatisticsConfiguration<a name="aws-properties-databrew-job-statisticsconfiguration"></a>

Configuration of evaluations for a profile job\. This configuration can be used to select evaluations and override the parameters of selected evaluations\. 

## Syntax<a name="aws-properties-databrew-job-statisticsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-job-statisticsconfiguration-syntax.json"></a>

```
{
  "[IncludedStatistics](#cfn-databrew-job-statisticsconfiguration-includedstatistics)" : [ String, ... ],
  "[Overrides](#cfn-databrew-job-statisticsconfiguration-overrides)" : [ StatisticOverride, ... ]
}
```

### YAML<a name="aws-properties-databrew-job-statisticsconfiguration-syntax.yaml"></a>

```
  [IncludedStatistics](#cfn-databrew-job-statisticsconfiguration-includedstatistics): 
    - String
  [Overrides](#cfn-databrew-job-statisticsconfiguration-overrides): 
    - StatisticOverride
```

## Properties<a name="aws-properties-databrew-job-statisticsconfiguration-properties"></a>

`IncludedStatistics`  <a name="cfn-databrew-job-statisticsconfiguration-includedstatistics"></a>
List of included evaluations\. When the list is undefined, all supported evaluations will be included\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Overrides`  <a name="cfn-databrew-job-statisticsconfiguration-overrides"></a>
List of overrides for evaluations\.  
*Required*: No  
*Type*: List of [StatisticOverride](aws-properties-databrew-job-statisticoverride.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)