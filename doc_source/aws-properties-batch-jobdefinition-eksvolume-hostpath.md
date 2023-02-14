# AWS::Batch::JobDefinition HostPath<a name="aws-properties-batch-jobdefinition-eksvolume-hostpath"></a>

Specifies the configuration of a Kubernetes `hostPath` volume\. A `hostPath` volume mounts an existing file or directory from the host node's filesystem into your pod\. For more information, see [hostPath](https://kubernetes.io/docs/concepts/storage/volumes/#hostpath) in the *Kubernetes documentation*\.

## Syntax<a name="aws-properties-batch-jobdefinition-eksvolume-hostpath-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-eksvolume-hostpath-syntax.json"></a>

```
{
  "[Path](#cfn-batch-jobdefinition-eksvolume-hostpath-path)" : String
}
```

### YAML<a name="aws-properties-batch-jobdefinition-eksvolume-hostpath-syntax.yaml"></a>

```
  [Path](#cfn-batch-jobdefinition-eksvolume-hostpath-path): String
```

## Properties<a name="aws-properties-batch-jobdefinition-eksvolume-hostpath-properties"></a>

`Path`  <a name="cfn-batch-jobdefinition-eksvolume-hostpath-path"></a>
The path of the file or directory on the host to mount into containers on the pod\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)