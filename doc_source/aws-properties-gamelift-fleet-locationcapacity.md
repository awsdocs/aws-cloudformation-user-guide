# AWS::GameLift::Fleet LocationCapacity<a name="aws-properties-gamelift-fleet-locationcapacity"></a>

Current resource capacity settings in a specified fleet or location\. The location value might refer to a fleet's remote location or its home Region\. 

 **Related actions** 

 [DescribeFleetCapacity](https://docs.aws.amazon.com/gamelift/latest/apireference/API_DescribeFleetCapacity.html) \| [DescribeFleetLocationCapacity](https://docs.aws.amazon.com/gamelift/latest/apireference/API_DescribeFleetLocationCapacity.html) \| [UpdateFleetCapacity](https://docs.aws.amazon.com/gamelift/latest/apireference/API_UpdateFleetCapacity.html) 

## Syntax<a name="aws-properties-gamelift-fleet-locationcapacity-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-gamelift-fleet-locationcapacity-syntax.json"></a>

```
{
  "[DesiredEC2Instances](#cfn-gamelift-fleet-locationcapacity-desiredec2instances)" : Integer,
  "[MaxSize](#cfn-gamelift-fleet-locationcapacity-maxsize)" : Integer,
  "[MinSize](#cfn-gamelift-fleet-locationcapacity-minsize)" : Integer
}
```

### YAML<a name="aws-properties-gamelift-fleet-locationcapacity-syntax.yaml"></a>

```
  [DesiredEC2Instances](#cfn-gamelift-fleet-locationcapacity-desiredec2instances): Integer
  [MaxSize](#cfn-gamelift-fleet-locationcapacity-maxsize): Integer
  [MinSize](#cfn-gamelift-fleet-locationcapacity-minsize): Integer
```

## Properties<a name="aws-properties-gamelift-fleet-locationcapacity-properties"></a>

`DesiredEC2Instances`  <a name="cfn-gamelift-fleet-locationcapacity-desiredec2instances"></a>
The number of Amazon EC2 instances you want to maintain in the specified fleet location\. This value must fall between the minimum and maximum size limits\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxSize`  <a name="cfn-gamelift-fleet-locationcapacity-maxsize"></a>
The maximum number of instances that are allowed in the specified fleet location\. If this parameter is not set, the default is 1\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinSize`  <a name="cfn-gamelift-fleet-locationcapacity-minsize"></a>
The minimum number of instances that are allowed in the specified fleet location\. If this parameter is not set, the default is 0\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)