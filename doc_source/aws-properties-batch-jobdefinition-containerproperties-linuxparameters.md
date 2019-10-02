# AWS::Batch::JobDefinition LinuxParameters<a name="aws-properties-batch-jobdefinition-containerproperties-linuxparameters"></a>

Linux\-specific modifications that are applied to the container, such as details for device mappings\.

## Syntax<a name="aws-properties-batch-jobdefinition-containerproperties-linuxparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-containerproperties-linuxparameters-syntax.json"></a>

```
{
  "[Devices](#cfn-batch-jobdefinition-containerproperties-linuxparameters-devices)" : [ [Device](aws-properties-batch-jobdefinition-device.md), ... ]
}
```

### YAML<a name="aws-properties-batch-jobdefinition-containerproperties-linuxparameters-syntax.yaml"></a>

```
  [Devices](#cfn-batch-jobdefinition-containerproperties-linuxparameters-devices): 
    - [Device](aws-properties-batch-jobdefinition-device.md)
```

## Properties<a name="aws-properties-batch-jobdefinition-containerproperties-linuxparameters-properties"></a>

`Devices`  <a name="cfn-batch-jobdefinition-containerproperties-linuxparameters-devices"></a>
Any host devices to expose to the container\. This parameter maps to `Devices` in the [Create a container](https://docs.docker.com/engine/api/v1.23/#create-a-container) section of the [Docker Remote API](https://docs.docker.com/engine/api/v1.23/) and the `--device` option to [docker run](https://docs.docker.com/engine/reference/run/)\.  
*Required*: No  
*Type*: List of [Device](aws-properties-batch-jobdefinition-device.md)  
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
