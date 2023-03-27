# AWS::AutoScaling::AutoScalingGroup LaunchTemplateOverrides<a name="aws-properties-autoscaling-autoscalinggroup-launchtemplateoverrides"></a>

Use this structure to let Amazon EC2 Auto Scaling do the following when the Auto Scaling group has a mixed instances policy:
+ Override the instance type that is specified in the launch template\.
+ Use multiple instance types\.

Specify the instance types that you want, or define your instance requirements instead and let Amazon EC2 Auto Scaling provision the available instance types that meet your requirements\. This can provide Amazon EC2 Auto Scaling with a larger selection of instance types to choose from when fulfilling Spot and On\-Demand capacities\. You can view which instance types are matched before you apply the instance requirements to your Auto Scaling group\.

After you define your instance requirements, you don't have to keep updating these settings to get new EC2 instance types automatically\. Amazon EC2 Auto Scaling uses the instance requirements of the Auto Scaling group to determine whether a new EC2 instance type can be used\.

 `LaunchTemplateOverrides` is a property of the [AWS::AutoScaling::AutoScalingGroup LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-launchtemplate.html) property type\.

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
The instance requirements\. Amazon EC2 Auto Scaling uses your specified requirements to identify instance types\. Then, it uses your On\-Demand and Spot allocation strategies to launch instances from these instance types\.  
You can specify up to four separate sets of instance requirements per Auto Scaling group\. This is useful for provisioning instances from different Amazon Machine Images \(AMIs\) in the same Auto Scaling group\. To do this, create the AMIs and create a new launch template for each AMI\. Then, create a compatible set of instance requirements for each launch template\.   
If you specify `InstanceRequirements`, you can't specify `InstanceType`\.
*Required*: No  
*Type*: [InstanceRequirements](aws-properties-autoscaling-autoscalinggroup-instancerequirements.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceType`  <a name="cfn-autoscaling-autoscalinggroup-launchtemplateoverrides-instancetype"></a>
The instance type, such as `m3.xlarge`\. You must specify an instance type that is supported in your requested Region and Availability Zones\. For more information, see [Instance types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html) in the *Amazon Elastic Compute Cloud User Guide*\.  
You can specify up to 40 instance types per Auto Scaling group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchTemplateSpecification`  <a name="cfn-autoscaling-autoscalinggroup-launchtemplateoverrides-launchtemplatespecification"></a>
Provides a launch template for the specified instance type or set of instance requirements\. For example, some instance types might require a launch template with a different AMI\. If not provided, Amazon EC2 Auto Scaling uses the launch template that's specified in the `LaunchTemplate` definition\. For more information, see [Specifying a different launch template for an instance type](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-mixed-instances-groups-launch-template-overrides.html) in the *Amazon EC2 Auto Scaling User Guide*\.   
You can specify up to 20 launch templates per Auto Scaling group\. The launch templates specified in the overrides and in the `LaunchTemplate` definition count towards this limit\.  
*Required*: No  
*Type*: [LaunchTemplateSpecification](aws-properties-autoscaling-autoscalinggroup-launchtemplatespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WeightedCapacity`  <a name="cfn-autoscaling-autoscalinggroup-launchtemplateoverrides-weightedcapacity"></a>
If you provide a list of instance types to use, you can specify the number of capacity units provided by each instance type in terms of virtual CPUs, memory, storage, throughput, or other relative performance characteristic\. When a Spot or On\-Demand Instance is launched, the capacity units count toward the desired capacity\. Amazon EC2 Auto Scaling launches instances until the desired capacity is totally fulfilled, even if this results in an overage\. For example, if there are two units remaining to fulfill capacity, and Amazon EC2 Auto Scaling can only launch an instance with a `WeightedCapacity` of five units, the instance is launched, and the desired capacity is exceeded by three units\. For more information, see [Configure instance weighting for Amazon EC2 Auto Scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/ec2-auto-scaling-mixed-instances-groups-instance-weighting.html) in the *Amazon EC2 Auto Scaling User Guide*\. Value must be in the range of 1\-999\.   
If you specify a value for `WeightedCapacity` for one instance type, you must specify a value for `WeightedCapacity` for all of them\.  
Every Auto Scaling group has three size parameters \(`DesiredCapacity`, `MaxSize`, and `MinSize`\)\. Usually, you set these sizes based on a specific number of instances\. However, if you configure a mixed instances policy that defines weights for the instance types, you must specify these sizes with the same units that you use for weighting instances\. 
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)