# AWS::Batch::JobDefinition Tmpfs<a name="aws-properties-batch-jobdefinition-tmpfs"></a>

The container path, mount options, and size of the tmpfs mount\.

**Note**  
This object isn't applicable to jobs running on Fargate resources\.

## Syntax<a name="aws-properties-batch-jobdefinition-tmpfs-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-tmpfs-syntax.json"></a>

```
{
  "[ContainerPath](#cfn-batch-jobdefinition-tmpfs-containerpath)" : String,
  "[MountOptions](#cfn-batch-jobdefinition-tmpfs-mountoptions)" : [ String, ... ],
  "[Size](#cfn-batch-jobdefinition-tmpfs-size)" : Integer
}
```

### YAML<a name="aws-properties-batch-jobdefinition-tmpfs-syntax.yaml"></a>

```
  [ContainerPath](#cfn-batch-jobdefinition-tmpfs-containerpath): String
  [MountOptions](#cfn-batch-jobdefinition-tmpfs-mountoptions): 
    - String
  [Size](#cfn-batch-jobdefinition-tmpfs-size): Integer
```

## Properties<a name="aws-properties-batch-jobdefinition-tmpfs-properties"></a>

`ContainerPath`  <a name="cfn-batch-jobdefinition-tmpfs-containerpath"></a>
The absolute file path in the container where the tmpfs volume is mounted\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MountOptions`  <a name="cfn-batch-jobdefinition-tmpfs-mountoptions"></a>
The list of tmpfs volume mount options\.  
Valid values: "`defaults`" \| "`ro`" \| "`rw`" \| "`suid`" \| "`nosuid`" \| "`dev`" \| "`nodev`" \| "`exec`" \| "`noexec`" \| "`sync`" \| "`async`" \| "`dirsync`" \| "`remount`" \| "`mand`" \| "`nomand`" \| "`atime`" \| "`noatime`" \| "`diratime`" \| "`nodiratime`" \| "`bind`" \| "`rbind" | "unbindable" | "runbindable" | "private" | "rprivate" | "shared" | "rshared" | "slave" | "rslave" | "relatime`" \| "`norelatime`" \| "`strictatime`" \| "`nostrictatime`" \| "`mode`" \| "`uid`" \| "`gid`" \| "`nr_inodes`" \| "`nr_blocks`" \| "`mpol`"  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Size`  <a name="cfn-batch-jobdefinition-tmpfs-size"></a>
The size \(in MiB\) of the tmpfs volume\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)