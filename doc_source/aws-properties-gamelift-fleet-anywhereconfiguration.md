# AWS::GameLift::Fleet AnywhereConfiguration<a name="aws-properties-gamelift-fleet-anywhereconfiguration"></a>

GameLift Anywhere configuration options for your Anywhere fleets\.

## Syntax<a name="aws-properties-gamelift-fleet-anywhereconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-gamelift-fleet-anywhereconfiguration-syntax.json"></a>

```
{
  "[Cost](#cfn-gamelift-fleet-anywhereconfiguration-cost)" : String
}
```

### YAML<a name="aws-properties-gamelift-fleet-anywhereconfiguration-syntax.yaml"></a>

```
  [Cost](#cfn-gamelift-fleet-anywhereconfiguration-cost): String
```

## Properties<a name="aws-properties-gamelift-fleet-anywhereconfiguration-properties"></a>

`Cost`  <a name="cfn-gamelift-fleet-anywhereconfiguration-cost"></a>
The cost to run your fleet per hour\. GameLift uses the provided cost of your fleet to balance usage in queues\. For more information about queues, see [Setting up queues](https://docs.aws.amazon.com/gamelift/latest/developerguide/queues-intro.html) in the *Amazon GameLift Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `11`  
*Pattern*: `^\d{1,5}(?:\.\d{1,5})?$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)