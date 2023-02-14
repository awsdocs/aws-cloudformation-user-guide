# AWS::Batch::JobDefinition EksVolume<a name="aws-properties-batch-jobdefinition-eksvolume"></a>

Specifies an Amazon EKS volume for a job definition\.

## Syntax<a name="aws-properties-batch-jobdefinition-eksvolume-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-eksvolume-syntax.json"></a>

```
{
  "[EmptyDir](#cfn-batch-jobdefinition-eksvolume-emptydir)" : EmptyDir,
  "[HostPath](#cfn-batch-jobdefinition-eksvolume-hostpath)" : HostPath,
  "[Name](#cfn-batch-jobdefinition-eksvolume-name)" : String,
  "[Secret](#cfn-batch-jobdefinition-eksvolume-secret)" : Secret
}
```

### YAML<a name="aws-properties-batch-jobdefinition-eksvolume-syntax.yaml"></a>

```
  [EmptyDir](#cfn-batch-jobdefinition-eksvolume-emptydir): 
    EmptyDir
  [HostPath](#cfn-batch-jobdefinition-eksvolume-hostpath): 
    HostPath
  [Name](#cfn-batch-jobdefinition-eksvolume-name): String
  [Secret](#cfn-batch-jobdefinition-eksvolume-secret): 
    Secret
```

## Properties<a name="aws-properties-batch-jobdefinition-eksvolume-properties"></a>

`EmptyDir`  <a name="cfn-batch-jobdefinition-eksvolume-emptydir"></a>
Specifies the configuration of a Kubernetes `emptyDir` volume\. For more information, see [emptyDir](https://kubernetes.io/docs/concepts/storage/volumes/#emptydir) in the *Kubernetes documentation*\.  
*Required*: No  
*Type*: [EmptyDir](aws-properties-batch-jobdefinition-eksvolume-emptydir.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HostPath`  <a name="cfn-batch-jobdefinition-eksvolume-hostpath"></a>
Specifies the configuration of a Kubernetes `hostPath` volume\. For more information, see [hostPath](https://kubernetes.io/docs/concepts/storage/volumes/#hostpath) in the *Kubernetes documentation*\.  
*Required*: No  
*Type*: [HostPath](aws-properties-batch-jobdefinition-eksvolume-hostpath.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-batch-jobdefinition-eksvolume-name"></a>
The name of the volume\. The name must be allowed as a DNS subdomain name\. For more information, see [DNS subdomain names](https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#dns-subdomain-names) in the *Kubernetes documentation*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Secret`  <a name="cfn-batch-jobdefinition-eksvolume-secret"></a>
Specifies the configuration of a Kubernetes `secret` volume\. For more information, see [secret](https://kubernetes.io/docs/concepts/storage/volumes/#secret) in the *Kubernetes documentation*\.  
*Required*: No  
*Type*: [Secret](aws-properties-batch-jobdefinition-secret.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)