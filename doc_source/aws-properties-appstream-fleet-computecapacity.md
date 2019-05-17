# AWS::AppStream::Fleet ComputeCapacity<a name="aws-properties-appstream-fleet-computecapacity"></a>

The desired capacity for a fleet\.

## Syntax<a name="aws-properties-appstream-fleet-computecapacity-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appstream-fleet-computecapacity-syntax.json"></a>

```
{
  "[DesiredInstances](#cfn-appstream-fleet-computecapacity-desiredinstances)" : Integer
}
```

### YAML<a name="aws-properties-appstream-fleet-computecapacity-syntax.yaml"></a>

```
  [DesiredInstances](#cfn-appstream-fleet-computecapacity-desiredinstances): Integer
```

## Properties<a name="aws-properties-appstream-fleet-computecapacity-properties"></a>

`DesiredInstances`  <a name="cfn-appstream-fleet-computecapacity-desiredinstances"></a>
The desired number of streaming instances\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)