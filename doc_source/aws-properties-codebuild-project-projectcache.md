# AWS CodeBuild Project ProjectCache<a name="aws-properties-codebuild-project-projectcache"></a>

<a name="aws-properties-codebuild-project-projectcache-description"></a>The `ProjectCache` property type specifies settings that AWS CodeBuild uses to store and reuse build dependencies\.

<a name="aws-properties-codebuild-project-projectcache-inheritance"></a> `ProjectCache` is the property type for the `Cache` property of the [AWS::CodeBuild::Project](aws-resource-codebuild-project.md) resource\.

## Syntax<a name="aws-properties-codebuild-project-projectcache-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-project-projectcache-syntax.json"></a>

```
{
  "[Location](#cfn-codebuild-project-projectcache-location)" : String,
  "[Modes](#cfn-codebuild-project-projectcache-modes)" : [String, ...],                
  "[Type](#cfn-codebuild-project-projectcache-type)" : String
}
```

### YAML<a name="aws-properties-codebuild-project-projectcache-syntax.yaml"></a>

```
[Location](#cfn-codebuild-project-projectcache-location): String
[Modes](#cfn-codebuild-project-projectcache-modes): 
 - String
[Type](#cfn-codebuild-project-projectcache-type): String
```

## Properties<a name="aws-properties-codebuild-project-projectcache-properties"></a>

`Location`  <a name="cfn-codebuild-project-projectcache-location"></a>
Information about the cache location:   
+ `NO_CACHE` or `LOCAL`: This value is ignored\.
+ `S3`: This is the S3 bucket name/prefix\.
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Modes`  <a name="cfn-codebuild-project-projectcache-modes"></a>
 If you use a `LOCAL` cache, the local cache mode\. You can use one or more local cache modes at the same time\.   
+  `LOCAL_SOURCE_CACHE` mode caches Git metadata for primary and secondary sources\. After the cache is created, subsequent builds pull only the change between commits\. This mode is a good choice for projects with a clean working directory and a source that is a large Git repository\. If you choose this option and your project does not use a Git repository \(GitHub, GitHub Enterprise, or Bitbucket\), the option is ignored\. 
+  `LOCAL_DOCKER_LAYER_CACHE` mode caches existing Docker layers\. This mode is a good choice for projects that build or pull large Docker images\. It can prevent the performance issues caused by pulling large Docker images down from the network\. 
**Note**  
 You can use a Docker layer cache in the Linux enviornment only\. 
 The `privileged` flag must be set so that your project has the required Docker permissions\. 
 You should consider the security implications before you use a Docker layer cache\. 
+  `LOCAL_CUSTOM_CACHE` mode caches directories you specify in the buildspec file\. This mode is a good choice if your build scenario is not suited to one of the other three local cache modes\. If you use a custom cache: 
  +  Only directories can be specified for caching\. You cannot specify individual files\. 
  +  Symlinks are used to reference cached directories\. 
  +  Cached directories are linked to your build before it downloads its project sources\. Cached items are overriden if a source item has the same name\. Directories are specified using cache paths in the buildspec file\. 
*Required*: No  
 *Type*: An array of strings\.   
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Type`  <a name="cfn-codebuild-project-projectcache-type"></a>
The type of cache used by the build project\. Valid values include:  
+ `NO_CACHE`: The build project does not use any cache\.
+ `S3`: The build project reads and writes from and to S3\.
+ `LOCAL`: The build project stores a cache locally on a build host that is only available to that build host\.
*Required*: Yes  
 *Type*: *String*  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-codebuild-project-projectcache-seealso"></a>
+ [ ProjectCache](https://docs.aws.amazon.com/codebuild/latest/APIReference/API_ProjectCache.html) in the *AWS CodeBuild API Reference*