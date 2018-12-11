# Amazon AppStream 2\.0 Fleet ComputeCapacity<a name="aws-properties-appstream-fleet-computecapacity"></a>

<a name="aws-properties-appstream-fleet-computecapacity-description"></a>The `ComputeCapacity` property type specifies the desired capacity for an Amazon AppStream 2\.0 fleet\.

<a name="aws-properties-appstream-fleet-computecapacity-inheritance"></a> `ComputeCapacity` is a property of the [AWS::AppStream::Fleet](aws-resource-appstream-fleet.md) resource\.

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
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 