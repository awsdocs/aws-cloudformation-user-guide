# AWS Batch JobDefinition VolumesHost<a name="aws-properties-batch-jobdefinition-volumeshost"></a>

The `VolumesHost` property type specifies whether your data volume persists on the host container instance and where it is stored\. If the host parameter is empty, then the Docker daemon assigns a host path for your data volume, but the data is not guaranteed to persist after the containers associated with it stop running\.

## Syntax<a name="aws-properties-batch-jobdefinition-volumeshost-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-volumeshost-syntax.json"></a>

```
{
  "[SourcePath](#cfn-batch-jobdefinition-volumeshost-sourcepath)" : String
}
```

### YAML<a name="aws-properties-batch-jobdefinition-volumeshost-syntax.yaml"></a>

```
[SourcePath](#cfn-batch-jobdefinition-volumeshost-sourcepath): String
```

## Properties<a name="aws-properties-batch-jobdefinition-volumeshost-properties"></a>

`SourcePath`  <a name="cfn-batch-jobdefinition-volumeshost-sourcepath"></a>
The path on the host container instance that is presented to the container\. If this parameter is empty, then the Docker daemon has assigned a host path for you\. If the `VolumesHost` parameter contains a `SourcePath` file location, then the data volume persists at the specified location on the host container instance until you delete it manually\. If the `SourcePath` value does not exist on the host container instance, the Docker daemon creates it\. If the location does exist, the contents of the source path folder are exported\.  
 *Required*: no  
*Type*: String  
 *Update requires*: No Interruption 