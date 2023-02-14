# AWS::AutoScaling::AutoScalingGroup LaunchTemplateOverrides<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides"></a>

 `LaunchTemplateOverrides` is a property of the [AWS::AutoScaling::AutoScalingGroup LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-launchtemplate.html) property type that describes an override for a launch template\.

If you supply your own instance types, the maximum number of instance types that can be associated with an Auto Scaling group is 40\. The maximum number of distinct launch templates you can define for an Auto Scaling group is 20\. 

## Syntax<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides-syntax.json"></a>

```
{
  "[InstanceRequirements](#cfn-as-mixedinstancespolicy-instancerequirements)" : InstanceRequirements,
  "[InstanceType](#cfn-autoscaling-autoscalinggroup-launchtemplateoverrides-instancetype)" : String,
  "[LaunchTemplateSpecification](#cfn-autoscaling-autoscalinggroup-launchtemplateoverrides-launchtemplatespecification)" : LaunchTemplateSpecification,
  "[WeightedCapacity](#cfn-autoscaling-autoscalinggroup-launchtemplateoverrides-weightedcapacity)" : String
}
```

### YAML<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides-syntax.yaml"></a>

```
  [InstanceRequirements](#cfn-as-mixedinstancespolicy-instancerequirements): 
    InstanceRequirements
  [InstanceType](#cfn-autoscaling-autoscalinggroup-launchtemplateoverrides-instancetype): String
  [LaunchTemplateSpecification](#cfn-autoscaling-autoscalinggroup-launchtemplateoverrides-launchtemplatespecification): 
    LaunchTemplateSpecification
  [WeightedCapacity](#cfn-autoscaling-autoscalinggroup-launchtemplateoverrides-weightedcapacity): String
```

## Properties<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides-properties"></a>

`InstanceRequirements`  <a name="cfn-as-mixedinstancespolicy-instancerequirements"></a>
The instance requirements\. When you specify instance requirements, Amazon EC2 Auto Scaling finds instance types that satisfy your requirements, and then uses your On\-Demand and Spot allocation strategies to launch instances from these instance types, in the same way as when you specify a list of specific instance types\.   
`InstanceRequirements` are incompatible with the `InstanceType` property\. If you specify both of these properties, Amazon EC2 Auto Scaling will return a `ValidationException` exception\. 
*Required*: No  
*Type*: [InstanceRequirements](aws-properties-autoscaling-autoscalinggroup-instancerequirements.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceType`  <a name="cfn-autoscaling-autoscalinggroup-launchtemplateoverrides-instancetype"></a>
The instance type, such as `m3.xlarge`\. You must use an instance type that is supported in your requested Region and Availability Zones\. For more information, see [Available instance types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#AvailableInstanceTypes) in the *Amazon EC2 User Guide for Linux Instances\.*   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchTemplateSpecification`  <a name="cfn-autoscaling-autoscalinggroup-launchtemplateoverrides-launchtemplatespecification"></a>
Provides a launch template for the specified instance type or instance requirements\. For example, some instance types might require a launch template with a different AMI\. If not provided, Amazon EC2 Auto Scaling uses the launch template that's defined for your mixed instances policy\. For more information, see [Specifying a different launch template for an instance type](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-mixed-instances-groups-launch-template-overrides.html) in the *Amazon EC2 Auto Scaling User Guide*\.   
*Required*: No  
*Type*: [LaunchTemplateSpecification](aws-properties-autoscaling-autoscalinggroup-launchtemplatespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WeightedCapacity`  <a name="cfn-autoscaling-autoscalinggroup-launchtemplateoverrides-weightedcapacity"></a>
The number of capacity units provided by the instance type specified in `InstanceType` in terms of virtual CPUs, memory, storage, throughput, or other relative performance characteristic\. When a Spot or On\-Demand Instance is provisioned, the capacity units count toward the desired capacity\. Amazon EC2 Auto Scaling provisions instances until the desired capacity is totally fulfilled, even if this results in an overage\. For example, if there are 2 units remaining to fulfill capacity, and Amazon EC2 Auto Scaling can only provision an instance with a `WeightedCapacity` of 5 units, the instance is provisioned, and the desired capacity is exceeded by 3 units\. For more information, see [Instance weighting for Amazon EC2 Auto Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-mixed-instances-groups-instance-weighting.html) in the *Amazon EC2 Auto Scaling User Guide*\. Value must be in the range of 1\-999\.   
Every Auto Scaling group has three size parameters \(`DesiredCapacity`, `MaxSize`, and `MinSize`\)\. Usually, you set these sizes based on a specific number of instances\. However, if you configure a mixed instances policy that defines weights for the instance types, you must specify these sizes with the same units that you use for weighting instances\. 
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)