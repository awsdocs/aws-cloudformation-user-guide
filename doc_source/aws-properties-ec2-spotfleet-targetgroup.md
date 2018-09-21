# Amazon EC2 SpotFleet TargetGroup<a name="aws-properties-ec2-spotfleet-targetgroup"></a>

<a name="aws-properties-ec2-spotfleet-targetgroup-description"></a>The `TargetGroup` property type describes a load balancer target group\.

<a name="aws-properties-ec2-spotfleet-targetgroup-inheritance"></a> `TargetGroup` is a property of the [Amazon EC2 SpotFleet TargetGroupsConfig](aws-properties-ec2-spotfleet-targetgroupsconfig.md) property type\.

## Syntax<a name="aws-properties-ec2-spotfleet-targetgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-targetgroup-syntax.json"></a>

```
{
  "[Arn](#cfn-ec2-spotfleet-targetgroup-arn)" : String
}
```

### YAML<a name="aws-properties-ec2-spotfleet-targetgroup-syntax.yaml"></a>

```
[Arn](#cfn-ec2-spotfleet-targetgroup-arn): String
```

## Properties<a name="aws-properties-ec2-spotfleet-targetgroup-properties"></a>

`Arn`  <a name="cfn-ec2-spotfleet-targetgroup-arn"></a>
The Amazon Resource Name \(ARN\) of the target group\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-ec2-spotfleet-targetgroup-seealso"></a>
+ [TargetGroup](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_TargetGroup.html) in the *Amazon EC2 API Reference*