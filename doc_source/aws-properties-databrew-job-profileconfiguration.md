# AWS::DataBrew::Job ProfileConfiguration<a name="aws-properties-databrew-job-profileconfiguration"></a>

Configuration for profile jobs\. Configuration can be used to select columns, do evaluations, and override default parameters of evaluations\. When configuration is undefined, the profile job will apply default settings to all supported columns\. 

## Syntax<a name="aws-properties-databrew-job-profileconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-job-profileconfiguration-syntax.json"></a>

```
{
  "[ColumnStatisticsConfigurations](#cfn-databrew-job-profileconfiguration-columnstatisticsconfigurations)" : [ ColumnStatisticsConfiguration, ... ],
  "[DatasetStatisticsConfiguration](#cfn-databrew-job-profileconfiguration-datasetstatisticsconfiguration)" : StatisticsConfiguration,
  "[EntityDetectorConfiguration](#cfn-databrew-job-profileconfiguration-entitydetectorconfiguration)" : EntityDetectorConfiguration,
  "[ProfileColumns](#cfn-databrew-job-profileconfiguration-profilecolumns)" : [ ColumnSelector, ... ]
}
```

### YAML<a name="aws-properties-databrew-job-profileconfiguration-syntax.yaml"></a>

```
  [ColumnStatisticsConfigurations](#cfn-databrew-job-profileconfiguration-columnstatisticsconfigurations): 
    - ColumnStatisticsConfiguration
  [DatasetStatisticsConfiguration](#cfn-databrew-job-profileconfiguration-datasetstatisticsconfiguration): 
    StatisticsConfiguration
  [EntityDetectorConfiguration](#cfn-databrew-job-profileconfiguration-entitydetectorconfiguration): 
    EntityDetectorConfiguration
  [ProfileColumns](#cfn-databrew-job-profileconfiguration-profilecolumns): 
    - ColumnSelector
```

## Properties<a name="aws-properties-databrew-job-profileconfiguration-properties"></a>

`ColumnStatisticsConfigurations`  <a name="cfn-databrew-job-profileconfiguration-columnstatisticsconfigurations"></a>
List of configurations for column evaluations\. ColumnStatisticsConfigurations are used to select evaluations and override parameters of evaluations for particular columns\. When ColumnStatisticsConfigurations is undefined, the profile job will profile all supported columns and run all supported evaluations\.   
*Required*: No  
*Type*: List of [ColumnStatisticsConfiguration](aws-properties-databrew-job-columnstatisticsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatasetStatisticsConfiguration`  <a name="cfn-databrew-job-profileconfiguration-datasetstatisticsconfiguration"></a>
Configuration for inter\-column evaluations\. Configuration can be used to select evaluations and override parameters of evaluations\. When configuration is undefined, the profile job will run all supported inter\-column evaluations\.   
*Required*: No  
*Type*: [StatisticsConfiguration](aws-properties-databrew-job-statisticsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EntityDetectorConfiguration`  <a name="cfn-databrew-job-profileconfiguration-entitydetectorconfiguration"></a>
Configuration of entity detection for a profile job\. When undefined, entity detection is disabled\.  
*Required*: No  
*Type*: [EntityDetectorConfiguration](aws-properties-databrew-job-entitydetectorconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProfileColumns`  <a name="cfn-databrew-job-profileconfiguration-profilecolumns"></a>
List of column selectors\. ProfileColumns can be used to select columns from the dataset\. When ProfileColumns is undefined, the profile job will profile all supported columns\.   
*Required*: No  
*Type*: List of [ColumnSelector](aws-properties-databrew-job-columnselector.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)