# AWS::ImageBuilder::ImagePipeline EcrConfiguration<a name="aws-properties-imagebuilder-imagepipeline-ecrconfiguration"></a>

Settings that Image Builder uses to configure the ECR repository and the output container images that Amazon Inspector scans\.

## Syntax<a name="aws-properties-imagebuilder-imagepipeline-ecrconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-imagebuilder-imagepipeline-ecrconfiguration-syntax.json"></a>

```
{
  "[ContainerTags](#cfn-imagebuilder-imagepipeline-ecrconfiguration-containertags)" : [ String, ... ],
  "[RepositoryName](#cfn-imagebuilder-imagepipeline-ecrconfiguration-repositoryname)" : String
}
```

### YAML<a name="aws-properties-imagebuilder-imagepipeline-ecrconfiguration-syntax.yaml"></a>

```
  [ContainerTags](#cfn-imagebuilder-imagepipeline-ecrconfiguration-containertags): 
    - String
  [RepositoryName](#cfn-imagebuilder-imagepipeline-ecrconfiguration-repositoryname): String
```

## Properties<a name="aws-properties-imagebuilder-imagepipeline-ecrconfiguration-properties"></a>

`ContainerTags`  <a name="cfn-imagebuilder-imagepipeline-ecrconfiguration-containertags"></a>
Tags for Image Builder to apply to the output container image that &INS; scans\. Tags can help you identify and manage your scanned images\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RepositoryName`  <a name="cfn-imagebuilder-imagepipeline-ecrconfiguration-repositoryname"></a>
The name of the container repository that Amazon Inspector scans to identify findings for your container images\. The name includes the path for the repository location\. If you don’t provide this information, Image Builder creates a repository in your account named `image-builder-image-scanning-repository` for vulnerability scans of your output container images\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)