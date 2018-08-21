# AWS Batch JobDefinition Volumes<a name="aws-properties-batch-jobdefinition-volumes"></a>

The `Volumes` property type specifies data volumes for containers to use in a job definition\.

## Syntax<a name="aws-properties-batch-jobdefinition-volumes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-volumes-syntax.json"></a>

```
{
  "[Host](#cfn-batch-jobdefinition-volumes-host)" : [*VolumesHost*](aws-properties-batch-jobdefinition-volumeshost.md),
  "[Name](#cfn-batch-jobdefinition-volumes-name)" : String
}
```

### YAML<a name="aws-properties-batch-jobdefinition-volumes-syntax.yaml"></a>

```
[Host](#cfn-batch-jobdefinition-volumes-host): 
  [*VolumesHost*](aws-properties-batch-jobdefinition-volumeshost.md)
[Name](#cfn-batch-jobdefinition-volumes-name): String
```

## Properties<a name="aws-properties-batch-jobdefinition-volumes-properties"></a>

`Host`  <a name="cfn-batch-jobdefinition-volumes-host"></a>
The contents of the `Host` parameter determine whether your data volume persists on the host container instance and where it is stored\. If the host parameter is empty, then the Docker daemon assigns a host path for your data volume, but the data is not guaranteed to persist after the containers associated with it stop running\.  
 *Required*: no  
 *Type*: [AWS Batch JobDefinition VolumesHost](aws-properties-batch-jobdefinition-volumeshost.md)  
 *Update requires*: No Interruption 

`Name`  <a name="cfn-batch-jobdefinition-volumes-name"></a>
The name of the volume\. Up to 255 letters \(uppercase and lowercase\), numbers, hyphens, and underscores are allowed\. This name is referenced in the `SourceVolume` parameter of container definition `MountPoints`\.  
 *Required*: no  
*Type*: String  
 *Update requires*: No Interruption 