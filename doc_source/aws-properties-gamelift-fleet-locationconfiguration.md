# AWS::GameLift::Fleet LocationConfiguration<a name="aws-properties-gamelift-fleet-locationconfiguration"></a>

A remote location where a multi\-location fleet can deploy EC2 instances for game hosting\. 

## Syntax<a name="aws-properties-gamelift-fleet-locationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-gamelift-fleet-locationconfiguration-syntax.json"></a>

```
{
  "[Location](#cfn-gamelift-fleet-locationconfiguration-location)" : String,
  "[LocationCapacity](#cfn-gamelift-fleet-locationconfiguration-locationcapacity)" : LocationCapacity
}
```

### YAML<a name="aws-properties-gamelift-fleet-locationconfiguration-syntax.yaml"></a>

```
  [Location](#cfn-gamelift-fleet-locationconfiguration-location): String
  [LocationCapacity](#cfn-gamelift-fleet-locationconfiguration-locationcapacity): 
    LocationCapacity
```

## Properties<a name="aws-properties-gamelift-fleet-locationconfiguration-properties"></a>

`Location`  <a name="cfn-gamelift-fleet-locationconfiguration-location"></a>
An AWS Region code, such as `us-west-2`\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `^[A-Za-z0-9\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LocationCapacity`  <a name="cfn-gamelift-fleet-locationconfiguration-locationcapacity"></a>
Current resource capacity settings in a specified fleet or location\. The location value might refer to a fleet's remote location or its home Region\.   
 **Related actions**   
 [DescribeFleetCapacity](https://docs.aws.amazon.com/gamelift/latest/apireference/API_DescribeFleetCapacity.html) \| [DescribeFleetLocationCapacity](https://docs.aws.amazon.com/gamelift/latest/apireference/API_DescribeFleetLocationCapacity.html) \| [UpdateFleetCapacity](https://docs.aws.amazon.com/gamelift/latest/apireference/API_UpdateFleetCapacity.html)   
*Required*: No  
*Type*: [LocationCapacity](aws-properties-gamelift-fleet-locationcapacity.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)