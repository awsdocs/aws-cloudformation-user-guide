# AWS::KafkaConnect::Connector AutoScaling<a name="aws-properties-kafkaconnect-connector-autoscaling"></a>

Specifies how the connector scales\.

## Syntax<a name="aws-properties-kafkaconnect-connector-autoscaling-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kafkaconnect-connector-autoscaling-syntax.json"></a>

```
{
  "[MaxWorkerCount](#cfn-kafkaconnect-connector-autoscaling-maxworkercount)" : Integer,
  "[McuCount](#cfn-kafkaconnect-connector-autoscaling-mcucount)" : Integer,
  "[MinWorkerCount](#cfn-kafkaconnect-connector-autoscaling-minworkercount)" : Integer,
  "[ScaleInPolicy](#cfn-kafkaconnect-connector-autoscaling-scaleinpolicy)" : ScaleInPolicy,
  "[ScaleOutPolicy](#cfn-kafkaconnect-connector-autoscaling-scaleoutpolicy)" : ScaleOutPolicy
}
```

### YAML<a name="aws-properties-kafkaconnect-connector-autoscaling-syntax.yaml"></a>

```
  [MaxWorkerCount](#cfn-kafkaconnect-connector-autoscaling-maxworkercount): Integer
  [McuCount](#cfn-kafkaconnect-connector-autoscaling-mcucount): Integer
  [MinWorkerCount](#cfn-kafkaconnect-connector-autoscaling-minworkercount): Integer
  [ScaleInPolicy](#cfn-kafkaconnect-connector-autoscaling-scaleinpolicy): 
    ScaleInPolicy
  [ScaleOutPolicy](#cfn-kafkaconnect-connector-autoscaling-scaleoutpolicy): 
    ScaleOutPolicy
```

## Properties<a name="aws-properties-kafkaconnect-connector-autoscaling-properties"></a>

`MaxWorkerCount`  <a name="cfn-kafkaconnect-connector-autoscaling-maxworkercount"></a>
The maximum number of workers allocated to the connector\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`McuCount`  <a name="cfn-kafkaconnect-connector-autoscaling-mcucount"></a>
The number of microcontroller units \(MCUs\) allocated to each connector worker\. The valid values are 1,2,4,8\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinWorkerCount`  <a name="cfn-kafkaconnect-connector-autoscaling-minworkercount"></a>
The minimum number of workers allocated to the connector\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScaleInPolicy`  <a name="cfn-kafkaconnect-connector-autoscaling-scaleinpolicy"></a>
The sacle\-in policy for the connector\.  
*Required*: Yes  
*Type*: [ScaleInPolicy](aws-properties-kafkaconnect-connector-scaleinpolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScaleOutPolicy`  <a name="cfn-kafkaconnect-connector-autoscaling-scaleoutpolicy"></a>
The sacle\-out policy for the connector\.  
*Required*: Yes  
*Type*: [ScaleOutPolicy](aws-properties-kafkaconnect-connector-scaleoutpolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)