# AWS::SageMaker::Endpoint CapacitySize<a name="aws-properties-sagemaker-endpoint-capacitysize"></a>

Currently, the `CapacitySize` API is not supported\.

## Syntax<a name="aws-properties-sagemaker-endpoint-capacitysize-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-endpoint-capacitysize-syntax.json"></a>

```
{
  "[Type](#cfn-sagemaker-endpoint-capacitysize-type)" : String,
  "[Value](#cfn-sagemaker-endpoint-capacitysize-value)" : Integer
}
```

### YAML<a name="aws-properties-sagemaker-endpoint-capacitysize-syntax.yaml"></a>

```
  [Type](#cfn-sagemaker-endpoint-capacitysize-type): String
  [Value](#cfn-sagemaker-endpoint-capacitysize-value): Integer
```

## Properties<a name="aws-properties-sagemaker-endpoint-capacitysize-properties"></a>

`Type`  <a name="cfn-sagemaker-endpoint-capacitysize-type"></a>
This API is not supported\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CAPACITY_PERCENT | INSTANCE_COUNT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-sagemaker-endpoint-capacitysize-value"></a>
  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)