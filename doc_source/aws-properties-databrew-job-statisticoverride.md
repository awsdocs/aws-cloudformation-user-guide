# AWS::DataBrew::Job StatisticOverride<a name="aws-properties-databrew-job-statisticoverride"></a>

Override of a particular evaluation for a profile job\. 

## Syntax<a name="aws-properties-databrew-job-statisticoverride-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-job-statisticoverride-syntax.json"></a>

```
{
  "[Parameters](#cfn-databrew-job-statisticoverride-parameters)" : {Key : Value, ...},
  "[Statistic](#cfn-databrew-job-statisticoverride-statistic)" : String
}
```

### YAML<a name="aws-properties-databrew-job-statisticoverride-syntax.yaml"></a>

```
  [Parameters](#cfn-databrew-job-statisticoverride-parameters): 
    Key : Value
  [Statistic](#cfn-databrew-job-statisticoverride-statistic): String
```

## Properties<a name="aws-properties-databrew-job-statisticoverride-properties"></a>

`Parameters`  <a name="cfn-databrew-job-statisticoverride-parameters"></a>
A map that includes overrides of an evaluation’s parameters\.  
*Required*: Yes  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Statistic`  <a name="cfn-databrew-job-statisticoverride-statistic"></a>
The name of an evaluation  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[A-Z\_]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)