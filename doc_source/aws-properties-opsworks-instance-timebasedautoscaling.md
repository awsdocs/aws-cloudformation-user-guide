# AWS OpsWorks TimeBasedAutoScaling Type<a name="aws-properties-opsworks-instance-timebasedautoscaling"></a>

Describes the automatic time\-based scaling configuration for an [AWS::OpsWorks::Instance](aws-resource-opsworks-instance.md) resource type\. For more information, see [SetTimeBasedAutoScaling](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_SetTimeBasedAutoScaling.html) in the *AWS OpsWorks Stacks API Reference*\.

## Syntax<a name="w3ab2c21c14e1403b5"></a>

### JSON<a name="aws-properties-opsworks-instance-timebasedautoscaling-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-timebasedautoscaling-friday)" : { Integer : String, ... },
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-timebasedautoscaling-monday)" : { Integer : String, ... },
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-timebasedautoscaling-saturday)" : { Integer : String, ... },
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-timebasedautoscaling-sunday)" : { Integer : String, ... },
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-timebasedautoscaling-thursday)" : { Integer : String, ... },
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-timebasedautoscaling-tuesday)" : { Integer : String, ... },
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-timebasedautoscaling-wednesday)" : { Integer : String, ... }
}
```

### YAML<a name="aws-properties-opsworks-instance-timebasedautoscaling-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-timebasedautoscaling-friday):
  Integer: String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-timebasedautoscaling-monday):
  Integer: String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-timebasedautoscaling-saturday):
  Integer: String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-timebasedautoscaling-sunday):
  Integer: String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-timebasedautoscaling-thursday):
  Integer: String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-timebasedautoscaling-tuesday):
  Integer: String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-instance-timebasedautoscaling-wednesday):
  Integer: String
```

## Properties<a name="w3ab2c21c14e1403b7"></a>

For each day of the week, the schedule consists of a set of key–value pairs, where the key is the time period \(a UTC hour\) of `0` – `23` and the value indicates whether the instance should be online \(`on`\) or offline \(`off`\) for the specified period\.

`Friday`  
The schedule for Friday\.  
*Required: *No  
*Type*: String to string map

`Monday`  
The schedule for Monday\.  
*Required: *No  
*Type*: String to string map

`Saturday`  
The schedule for Saturday\.  
*Required: *No  
*Type*: String to string map

`Sunday`  
The schedule for Sunday\.  
*Required: *No  
*Type*: String to string map

`Thursday`  
The schedule for Thursday\.  
*Required: *No  
*Type*: String to string map

`Tuesday`  
The schedule for Tuesday\.  
*Required: *No  
*Type*: String to string map

`Wednesday`  
The schedule for Wednesday\.  
*Required: *No  
*Type*: String to string map