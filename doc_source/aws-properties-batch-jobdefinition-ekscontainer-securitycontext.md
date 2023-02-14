# AWS::Batch::JobDefinition SecurityContext<a name="aws-properties-batch-jobdefinition-ekscontainer-securitycontext"></a>

The security context for a job\. For more information, see [Configure a security context for a pod or container](https://kubernetes.io/docs/tasks/configure-pod-container/security-context/) in the *Kubernetes documentation*\.

## Syntax<a name="aws-properties-batch-jobdefinition-ekscontainer-securitycontext-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-ekscontainer-securitycontext-syntax.json"></a>

```
{
  "[Privileged](#cfn-batch-jobdefinition-ekscontainer-securitycontext-privileged)" : Boolean,
  "[ReadOnlyRootFilesystem](#cfn-batch-jobdefinition-ekscontainer-securitycontext-readonlyrootfilesystem)" : Boolean,
  "[RunAsGroup](#cfn-batch-jobdefinition-ekscontainer-securitycontext-runasgroup)" : Integer,
  "[RunAsNonRoot](#cfn-batch-jobdefinition-ekscontainer-securitycontext-runasnonroot)" : Boolean,
  "[RunAsUser](#cfn-batch-jobdefinition-ekscontainer-securitycontext-runasuser)" : Integer
}
```

### YAML<a name="aws-properties-batch-jobdefinition-ekscontainer-securitycontext-syntax.yaml"></a>

```
  [Privileged](#cfn-batch-jobdefinition-ekscontainer-securitycontext-privileged): Boolean
  [ReadOnlyRootFilesystem](#cfn-batch-jobdefinition-ekscontainer-securitycontext-readonlyrootfilesystem): Boolean
  [RunAsGroup](#cfn-batch-jobdefinition-ekscontainer-securitycontext-runasgroup): Integer
  [RunAsNonRoot](#cfn-batch-jobdefinition-ekscontainer-securitycontext-runasnonroot): Boolean
  [RunAsUser](#cfn-batch-jobdefinition-ekscontainer-securitycontext-runasuser): Integer
```

## Properties<a name="aws-properties-batch-jobdefinition-ekscontainer-securitycontext-properties"></a>

`Privileged`  <a name="cfn-batch-jobdefinition-ekscontainer-securitycontext-privileged"></a>
When this parameter is `true`, the container is given elevated permissions on the host container instance\. The level of permissions are similar to the `root` user permissions\. The default value is `false`\. This parameter maps to `privileged` policy in the [Privileged pod security policies](https://kubernetes.io/docs/concepts/security/pod-security-policy/#privileged) in the *Kubernetes documentation*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReadOnlyRootFilesystem`  <a name="cfn-batch-jobdefinition-ekscontainer-securitycontext-readonlyrootfilesystem"></a>
When this parameter is `true`, the container is given read\-only access to its root file system\. The default value is `false`\. This parameter maps to `ReadOnlyRootFilesystem` policy in the [Volumes and file systems pod security policies](https://kubernetes.io/docs/concepts/security/pod-security-policy/#volumes-and-file-systems) in the *Kubernetes documentation*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RunAsGroup`  <a name="cfn-batch-jobdefinition-ekscontainer-securitycontext-runasgroup"></a>
When this parameter is specified, the container is run as the specified group ID \(`gid`\)\. If this parameter isn't specified, the default is the group that's specified in the image metadata\. This parameter maps to `RunAsGroup` and `MustRunAs` policy in the [Users and groups pod security policies](https://kubernetes.io/docs/concepts/security/pod-security-policy/#users-and-groups) in the *Kubernetes documentation*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RunAsNonRoot`  <a name="cfn-batch-jobdefinition-ekscontainer-securitycontext-runasnonroot"></a>
When this parameter is specified, the container is run as a user with a `uid` other than 0\. If this parameter isn't specified, so such rule is enforced\. This parameter maps to `RunAsUser` and `MustRunAsNonRoot` policy in the [Users and groups pod security policies](https://kubernetes.io/docs/concepts/security/pod-security-policy/#users-and-groups) in the *Kubernetes documentation*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RunAsUser`  <a name="cfn-batch-jobdefinition-ekscontainer-securitycontext-runasuser"></a>
When this parameter is specified, the container is run as the specified user ID \(`uid`\)\. If this parameter isn't specified, the default is the user that's specified in the image metadata\. This parameter maps to `RunAsUser` and `MustRanAs` policy in the [Users and groups pod security policies](https://kubernetes.io/docs/concepts/security/pod-security-policy/#users-and-groups) in the *Kubernetes documentation*\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)