# AWS::CodeBuild::Project ProjectFileSystemLocation<a name="aws-properties-codebuild-project-projectfilesystemlocation"></a>

 Information about a file system created by Amazon Elastic File System \(EFS\)\. For more information, see [What Is Amazon Elastic File System?](https://docs.aws.amazon.com/efs/latest/ug/whatisefs.html) 

## Syntax<a name="aws-properties-codebuild-project-projectfilesystemlocation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-project-projectfilesystemlocation-syntax.json"></a>

```
{
  "[Identifier](#cfn-codebuild-project-projectfilesystemlocation-identifier)" : String,
  "[Location](#cfn-codebuild-project-projectfilesystemlocation-location)" : String,
  "[MountOptions](#cfn-codebuild-project-projectfilesystemlocation-mountoptions)" : String,
  "[MountPoint](#cfn-codebuild-project-projectfilesystemlocation-mountpoint)" : String,
  "[Type](#cfn-codebuild-project-projectfilesystemlocation-type)" : String
}
```

### YAML<a name="aws-properties-codebuild-project-projectfilesystemlocation-syntax.yaml"></a>

```
  [Identifier](#cfn-codebuild-project-projectfilesystemlocation-identifier): String
  [Location](#cfn-codebuild-project-projectfilesystemlocation-location): String
  [MountOptions](#cfn-codebuild-project-projectfilesystemlocation-mountoptions): String
  [MountPoint](#cfn-codebuild-project-projectfilesystemlocation-mountpoint): String
  [Type](#cfn-codebuild-project-projectfilesystemlocation-type): String
```

## Properties<a name="aws-properties-codebuild-project-projectfilesystemlocation-properties"></a>

`Identifier`  <a name="cfn-codebuild-project-projectfilesystemlocation-identifier"></a>
The name used to access a file system created by Amazon EFS\. CodeBuild creates an environment variable by appending the `identifier` in all capital letters to `CODEBUILD_`\. For example, if you specify `my_efs` for `identifier`, a new environment variable is create named `CODEBUILD_MY_EFS`\.   
 The `identifier` is used to mount your file system\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Location`  <a name="cfn-codebuild-project-projectfilesystemlocation-location"></a>
A string that specifies the location of the file system created by Amazon EFS\. Its format is `efs-dns-name:/directory-path`\. You can find the DNS name of file system when you view it in the AWS EFS console\. The directory path is a path to a directory in the file system that CodeBuild mounts\. For example, if the DNS name of a file system is `fs-abcd1234.efs.us-west-2.amazonaws.com`, and its mount directory is `my-efs-mount-directory`, then the `location` is `fs-abcd1234.efs.us-west-2.amazonaws.com:/my-efs-mount-directory`\.   
The directory path in the format `efs-dns-name:/directory-path` is optional\. If you do not specify a directory path, the location is only the DNS name and CodeBuild mounts the entire file system\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MountOptions`  <a name="cfn-codebuild-project-projectfilesystemlocation-mountoptions"></a>
 The mount options for a file system created by AWS EFS\. The default mount options used by CodeBuild are `nfsvers=4.1,rsize=1048576,wsize=1048576,hard,timeo=600,retrans=2`\. For more information, see [Recommended NFS Mount Options](https://docs.aws.amazon.com/efs/latest/ug/mounting-fs-nfs-mount-settings.html)\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MountPoint`  <a name="cfn-codebuild-project-projectfilesystemlocation-mountpoint"></a>
The location in the container where you mount the file system\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-codebuild-project-projectfilesystemlocation-type"></a>
 The type of the file system\. The one supported type is `EFS`\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `EFS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)