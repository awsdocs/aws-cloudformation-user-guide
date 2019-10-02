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

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `us-east-1`
- `us-west-2`
