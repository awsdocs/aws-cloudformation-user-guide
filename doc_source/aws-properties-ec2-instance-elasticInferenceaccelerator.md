# Amazon Elastic Compute Cloud Instance ElasticInferenceAccelerator<a name="aws-properties-ec2-instance-elasticInferenceaccelerator"></a>

<a name="aws-properties-ec2-instance-elasticInferenceaccelerator-description"></a>The `ElasticInferenceAccelerator` property type specifies an elastic inference accelerator for an instance\. Elastic Inference \(EI\) accelerators are a resource you can attach to your Amazon EC2 instances to accelerate your Deep Learning \(DL\) inference workloads\.

<a name="aws-properties-ec2-instance-elasticInferenceaccelerator-inheritance"></a> `ElasticInferenceAccelerator` is a property of the [AWS::EC2::Instance](aws-properties-ec2-instance.md) resource\.

## Syntax<a name="aws-properties-ec2-instance-elasticInferenceaccelerator-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-instance-elasticInferenceaccelerator-syntax.json"></a>

```
{
  "[Type](#cfn-ec2-instance-elasticInferenceaccelerator-type)" : String
}
```

### YAML<a name="aws-properties-ec2-instance-elasticInferenceaccelerator-syntax.yaml"></a>

```
[Type](#cfn-ec2-instance-elasticInferenceaccelerator-type): String
```

## Properties<a name="aws-properties-ec2-instance-elasticInferenceaccelerator-properties"></a>

`Type`  <a name="cfn-ec2-instance-elasticInferenceaccelerator-type"></a>
The type of elastic inference accelerator\. The possible values are `eia1.medium`, `eia1.large`, and `eia1.xlarge`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 