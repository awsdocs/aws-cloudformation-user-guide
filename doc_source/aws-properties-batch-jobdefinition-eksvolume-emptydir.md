# AWS::Batch::JobDefinition EmptyDir<a name="aws-properties-batch-jobdefinition-eksvolume-emptydir"></a>

Specifies the configuration of a Kubernetes `emptyDir` volume\. An `emptyDir` volume is first created when a pod is assigned to a node\. It exists as long as that pod is running on that node\. The `emptyDir` volume is initially empty\. All containers in the pod can read and write the files in the `emptyDir` volume\. However, the `emptyDir` volume can be mounted at the same or different paths in each container\. When a pod is removed from a node for any reason, the data in the `emptyDir` is deleted permanently\. For more information, see [emptyDir](https://kubernetes.io/docs/concepts/storage/volumes/#emptydir) in the *Kubernetes documentation*\.

## Syntax<a name="aws-properties-batch-jobdefinition-eksvolume-emptydir-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-eksvolume-emptydir-syntax.json"></a>

```
{
  "[Medium](#cfn-batch-jobdefinition-eksvolume-emptydir-medium)" : String,
  "[SizeLimit](#cfn-batch-jobdefinition-eksvolume-emptydir-sizelimit)" : String
}
```

### YAML<a name="aws-properties-batch-jobdefinition-eksvolume-emptydir-syntax.yaml"></a>

```
  [Medium](#cfn-batch-jobdefinition-eksvolume-emptydir-medium): String
  [SizeLimit](#cfn-batch-jobdefinition-eksvolume-emptydir-sizelimit): String
```

## Properties<a name="aws-properties-batch-jobdefinition-eksvolume-emptydir-properties"></a>

`Medium`  <a name="cfn-batch-jobdefinition-eksvolume-emptydir-medium"></a>
The medium to store the volume\. The default value is an empty string, which uses the storage of the node\.    
""  
 **\(Default\)** Use the disk storage of the node\.  
"Memory"  
Use the `tmpfs` volume that's backed by the RAM of the node\. Contents of the volume are lost when the node reboots, and any storage on the volume counts against the container's memory limit\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SizeLimit`  <a name="cfn-batch-jobdefinition-eksvolume-emptydir-sizelimit"></a>
The maximum size of the volume\. By default, there's no maximum size defined\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)