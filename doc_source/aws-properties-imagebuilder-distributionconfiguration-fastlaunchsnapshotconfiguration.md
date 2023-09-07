# AWS::ImageBuilder::DistributionConfiguration FastLaunchSnapshotConfiguration<a name="aws-properties-imagebuilder-distributionconfiguration-fastlaunchsnapshotconfiguration"></a>

Configuration settings for creating and managing pre\-provisioned snapshots for a fast\-launch enabled Windows AMI\.

## Syntax<a name="aws-properties-imagebuilder-distributionconfiguration-fastlaunchsnapshotconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-imagebuilder-distributionconfiguration-fastlaunchsnapshotconfiguration-syntax.json"></a>

```
{
  "[TargetResourceCount](#cfn-imagebuilder-distributionconfiguration-fastlaunchsnapshotconfiguration-targetresourcecount)" : Integer
}
```

### YAML<a name="aws-properties-imagebuilder-distributionconfiguration-fastlaunchsnapshotconfiguration-syntax.yaml"></a>

```
  [TargetResourceCount](#cfn-imagebuilder-distributionconfiguration-fastlaunchsnapshotconfiguration-targetresourcecount): Integer
```

## Properties<a name="aws-properties-imagebuilder-distributionconfiguration-fastlaunchsnapshotconfiguration-properties"></a>

`TargetResourceCount`  <a name="cfn-imagebuilder-distributionconfiguration-fastlaunchsnapshotconfiguration-targetresourcecount"></a>
The number of pre\-provisioned snapshots to keep on hand for a fast\-launch enabled Windows AMI\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `10000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)