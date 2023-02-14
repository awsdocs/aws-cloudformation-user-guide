# AWS::KafkaConnect::Connector ScaleInPolicy<a name="aws-properties-kafkaconnect-connector-scaleinpolicy"></a>

The scale\-in policy for the connector\.

## Syntax<a name="aws-properties-kafkaconnect-connector-scaleinpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kafkaconnect-connector-scaleinpolicy-syntax.json"></a>

```
{
  "[CpuUtilizationPercentage](#cfn-kafkaconnect-connector-scaleinpolicy-cpuutilizationpercentage)" : Integer
}
```

### YAML<a name="aws-properties-kafkaconnect-connector-scaleinpolicy-syntax.yaml"></a>

```
  [CpuUtilizationPercentage](#cfn-kafkaconnect-connector-scaleinpolicy-cpuutilizationpercentage): Integer
```

## Properties<a name="aws-properties-kafkaconnect-connector-scaleinpolicy-properties"></a>

`CpuUtilizationPercentage`  <a name="cfn-kafkaconnect-connector-scaleinpolicy-cpuutilizationpercentage"></a>
Specifies the CPU utilization percentage threshold at which you want connector scale in to be triggered\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)