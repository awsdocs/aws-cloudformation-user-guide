# AWS::GameLift::GameServerGroup InstanceDefinitions<a name="aws-properties-gamelift-gameservergroup-instancedefinitions"></a>

The set of EC2 instance types that GameLift FleetIQ can use when balancing and automatically scaling instances in the corresponding Auto Scaling group\. 

## Syntax<a name="aws-properties-gamelift-gameservergroup-instancedefinitions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-gamelift-gameservergroup-instancedefinitions-syntax.json"></a>

```
{
  "[InstanceDefinitions](#cfn-gamelift-gameservergroup-instancedefinitions-instancedefinitions)" : [ InstanceDefinition, ... ]
}
```

### YAML<a name="aws-properties-gamelift-gameservergroup-instancedefinitions-syntax.yaml"></a>

```
  [InstanceDefinitions](#cfn-gamelift-gameservergroup-instancedefinitions-instancedefinitions): 
    - InstanceDefinition
```

## Properties<a name="aws-properties-gamelift-gameservergroup-instancedefinitions-properties"></a>

`InstanceDefinitions`  <a name="cfn-gamelift-gameservergroup-instancedefinitions-instancedefinitions"></a>
The set of EC2 instance types that GameLift FleetIQ can use when balancing and automatically scaling instances in the corresponding Auto Scaling group\.   
*Required*: No  
*Type*: [List](#aws-properties-gamelift-gameservergroup-instancedefinitions) of [InstanceDefinition](aws-properties-gamelift-gameservergroup-instancedefinition.md)  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)