# AWS::KafkaConnect::Connector ScaleOutPolicy<a name="aws-properties-kafkaconnect-connector-scaleoutpolicy"></a>

The scale\-out policy for the connector\.

## Syntax<a name="aws-properties-kafkaconnect-connector-scaleoutpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kafkaconnect-connector-scaleoutpolicy-syntax.json"></a>

```
{
  "[CpuUtilizationPercentage](#cfn-kafkaconnect-connector-scaleoutpolicy-cpuutilizationpercentage)" : Integer
}
```

### YAML<a name="aws-properties-kafkaconnect-connector-scaleoutpolicy-syntax.yaml"></a>

```
  [CpuUtilizationPercentage](#cfn-kafkaconnect-connector-scaleoutpolicy-cpuutilizationpercentage): Integer
```

## Properties<a name="aws-properties-kafkaconnect-connector-scaleoutpolicy-properties"></a>

`CpuUtilizationPercentage`  <a name="cfn-kafkaconnect-connector-scaleoutpolicy-cpuutilizationpercentage"></a>
The CPU utilization percentage threshold at which you want connector scale out to be triggered\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)