# AWS::Neptune::DBCluster ServerlessScalingConfiguration<a name="aws-properties-neptune-dbcluster-serverlessscalingconfiguration"></a>

Contains the scaling configuration of a Neptune Serverless DB cluster\.

## Syntax<a name="aws-properties-neptune-dbcluster-serverlessscalingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-neptune-dbcluster-serverlessscalingconfiguration-syntax.json"></a>

```
{
  "[MaxCapacity](#cfn-neptune-dbcluster-serverlessscalingconfiguration-maxcapacity)" : Double,
  "[MinCapacity](#cfn-neptune-dbcluster-serverlessscalingconfiguration-mincapacity)" : Double
}
```

### YAML<a name="aws-properties-neptune-dbcluster-serverlessscalingconfiguration-syntax.yaml"></a>

```
  [MaxCapacity](#cfn-neptune-dbcluster-serverlessscalingconfiguration-maxcapacity): Double
  [MinCapacity](#cfn-neptune-dbcluster-serverlessscalingconfiguration-mincapacity): Double
```

## Properties<a name="aws-properties-neptune-dbcluster-serverlessscalingconfiguration-properties"></a>

`MaxCapacity`  <a name="cfn-neptune-dbcluster-serverlessscalingconfiguration-maxcapacity"></a>
The maximum number of Neptune capacity units \(NCUs\) for a DB instance in a Neptune Serverless cluster\. You can specify NCU values in half\-step increments, such as 40, 40\.5, 41, and so on\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinCapacity`  <a name="cfn-neptune-dbcluster-serverlessscalingconfiguration-mincapacity"></a>
The minimum number of Neptune capacity units \(NCUs\) for a DB instance in a Neptune Serverless cluster\. You can specify NCU values in half\-step increments, such as 8, 8\.5, 9, and so on\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)