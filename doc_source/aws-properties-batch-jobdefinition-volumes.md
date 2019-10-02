# AWS::Batch::JobDefinition Volumes<a name="aws-properties-batch-jobdefinition-volumes"></a>

A list of volumes associated with the job\.

## Syntax<a name="aws-properties-batch-jobdefinition-volumes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-volumes-syntax.json"></a>

```
{
  "[Host](#cfn-batch-jobdefinition-volumes-host)" : [VolumesHost](aws-properties-batch-jobdefinition-volumeshost.md),
  "[Name](#cfn-batch-jobdefinition-volumes-name)" : String
}
```

### YAML<a name="aws-properties-batch-jobdefinition-volumes-syntax.yaml"></a>

```
  [Host](#cfn-batch-jobdefinition-volumes-host): 
    [VolumesHost](aws-properties-batch-jobdefinition-volumeshost.md)
  [Name](#cfn-batch-jobdefinition-volumes-name): String
```

## Properties<a name="aws-properties-batch-jobdefinition-volumes-properties"></a>

`Host`  <a name="cfn-batch-jobdefinition-volumes-host"></a>
The contents of the `host` parameter determine whether your data volume persists on the host container instance and where it is stored\. If the host parameter is empty, then the Docker daemon assigns a host path for your data volume\. However, the data is not guaranteed to persist after the containers associated with it stop running\.  
*Required*: No  
*Type*: [VolumesHost](aws-properties-batch-jobdefinition-volumeshost.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-batch-jobdefinition-volumes-name"></a>
The name of the volume\. Up to 255 letters \(uppercase and lowercase\), numbers, hyphens, and underscores are allowed\. This name is referenced in the `sourceVolume` parameter of container definition `mountPoints`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
