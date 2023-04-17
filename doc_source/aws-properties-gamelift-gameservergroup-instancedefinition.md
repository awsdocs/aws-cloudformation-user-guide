# AWS::GameLift::GameServerGroup InstanceDefinition<a name="aws-properties-gamelift-gameservergroup-instancedefinition"></a>

 **This data type is used with the Amazon GameLift FleetIQ and game server groups\.** 

An allowed instance type for a `GameServerGroup`\. All game server groups must have at least two instance types defined for it\. GameLift FleetIQ periodically evaluates each defined instance type for viability\. It then updates the Auto Scaling group with the list of viable instance types\.

## Syntax<a name="aws-properties-gamelift-gameservergroup-instancedefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-gamelift-gameservergroup-instancedefinition-syntax.json"></a>

```
{
  "[InstanceType](#cfn-gamelift-gameservergroup-instancedefinition-instancetype)" : String,
  "[WeightedCapacity](#cfn-gamelift-gameservergroup-instancedefinition-weightedcapacity)" : String
}
```

### YAML<a name="aws-properties-gamelift-gameservergroup-instancedefinition-syntax.yaml"></a>

```
  [InstanceType](#cfn-gamelift-gameservergroup-instancedefinition-instancetype): String
  [WeightedCapacity](#cfn-gamelift-gameservergroup-instancedefinition-weightedcapacity): String
```

## Properties<a name="aws-properties-gamelift-gameservergroup-instancedefinition-properties"></a>

`InstanceType`  <a name="cfn-gamelift-gameservergroup-instancedefinition-instancetype"></a>
An Amazon EC2 instance type designation\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `c4.2xlarge | c4.4xlarge | c4.8xlarge | c4.large | c4.xlarge | c5.12xlarge | c5.18xlarge | c5.24xlarge | c5.2xlarge | c5.4xlarge | c5.9xlarge | c5.large | c5.xlarge | c5a.12xlarge | c5a.16xlarge | c5a.24xlarge | c5a.2xlarge | c5a.4xlarge | c5a.8xlarge | c5a.large | c5a.xlarge | c6g.12xlarge | c6g.16xlarge | c6g.2xlarge | c6g.4xlarge | c6g.8xlarge | c6g.large | c6g.medium | c6g.xlarge | m4.10xlarge | m4.2xlarge | m4.4xlarge | m4.large | m4.xlarge | m5.12xlarge | m5.16xlarge | m5.24xlarge | m5.2xlarge | m5.4xlarge | m5.8xlarge | m5.large | m5.xlarge | m5a.12xlarge | m5a.16xlarge | m5a.24xlarge | m5a.2xlarge | m5a.4xlarge | m5a.8xlarge | m5a.large | m5a.xlarge | m6g.12xlarge | m6g.16xlarge | m6g.2xlarge | m6g.4xlarge | m6g.8xlarge | m6g.large | m6g.medium | m6g.xlarge | r4.16xlarge | r4.2xlarge | r4.4xlarge | r4.8xlarge | r4.large | r4.xlarge | r5.12xlarge | r5.16xlarge | r5.24xlarge | r5.2xlarge | r5.4xlarge | r5.8xlarge | r5.large | r5.xlarge | r5a.12xlarge | r5a.16xlarge | r5a.24xlarge | r5a.2xlarge | r5a.4xlarge | r5a.8xlarge | r5a.large | r5a.xlarge | r6g.12xlarge | r6g.16xlarge | r6g.2xlarge | r6g.4xlarge | r6g.8xlarge | r6g.large | r6g.medium | r6g.xlarge`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WeightedCapacity`  <a name="cfn-gamelift-gameservergroup-instancedefinition-weightedcapacity"></a>
Instance weighting that indicates how much this instance type contributes to the total capacity of a game server group\. Instance weights are used by Amazon GameLift FleetIQ to calculate the instance type's cost per unit hour and better identify the most cost\-effective options\. For detailed information on weighting instance capacity, see [Instance Weighting](https://docs.aws.amazon.com/autoscaling/ec2/userguide/asg-instance-weighting.html) in the *Amazon Elastic Compute Cloud Auto Scaling User Guide*\. Default value is "1"\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `3`  
*Pattern*: `^[\u0031-\u0039][\u0030-\u0039]{0,2}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)