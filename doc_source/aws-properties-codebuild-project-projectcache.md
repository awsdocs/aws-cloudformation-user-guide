# AWS CodeBuild Project ProjectCache<a name="aws-properties-codebuild-project-projectcache"></a>

<a name="aws-properties-codebuild-project-projectcache-description"></a>The `ProjectCache` property type specifies settings that AWS CodeBuild uses to store and reuse build dependencies\.

<a name="aws-properties-codebuild-project-projectcache-inheritance"></a> `ProjectCache` is the property type for the `Cache` property of the [AWS::CodeBuild::Project](aws-resource-codebuild-project.md) resource\.

## Syntax<a name="aws-properties-codebuild-project-projectcache-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codebuild-project-projectcache-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codebuild-project-projectcache-location)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codebuild-project-projectcache-type)" : String
}
```

### YAML<a name="aws-properties-codebuild-project-projectcache-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codebuild-project-projectcache-location): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codebuild-project-projectcache-type): String
```

## Properties<a name="aws-properties-codebuild-project-projectcache-properties"></a>

`Location`  
The Amazon S3 bucket name and prefix—for example, `mybucket/prefix`\. This value is ignored when `Type` is set to `NO_CACHE`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

`Type`  
The type of cache for the build project to use\. Valid values are:  

+ `NO_CACHE`: The build project doesn't use any cache\.

+ `S3`: The build project reads from and writes to Amazon S3\.
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

## See Also<a name="aws-properties-codebuild-project-projectcache-seealso"></a>

+ [ ProjectCache](http://docs.aws.amazon.com/codebuild/latest/APIReference/API_ProjectCache.html) in the *AWS CodeBuild API Reference*