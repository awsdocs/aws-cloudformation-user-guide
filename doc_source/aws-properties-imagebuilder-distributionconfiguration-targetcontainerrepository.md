# AWS::ImageBuilder::DistributionConfiguration TargetContainerRepository<a name="aws-properties-imagebuilder-distributionconfiguration-targetcontainerrepository"></a>

The container repository where the output container image is stored\.

## Syntax<a name="aws-properties-imagebuilder-distributionconfiguration-targetcontainerrepository-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-imagebuilder-distributionconfiguration-targetcontainerrepository-syntax.json"></a>

```
{
  "[RepositoryName](#cfn-imagebuilder-distributionconfiguration-targetcontainerrepository-repositoryname)" : String,
  "[Service](#cfn-imagebuilder-distributionconfiguration-targetcontainerrepository-service)" : String
}
```

### YAML<a name="aws-properties-imagebuilder-distributionconfiguration-targetcontainerrepository-syntax.yaml"></a>

```
  [RepositoryName](#cfn-imagebuilder-distributionconfiguration-targetcontainerrepository-repositoryname): String
  [Service](#cfn-imagebuilder-distributionconfiguration-targetcontainerrepository-service): String
```

## Properties<a name="aws-properties-imagebuilder-distributionconfiguration-targetcontainerrepository-properties"></a>

`RepositoryName`  <a name="cfn-imagebuilder-distributionconfiguration-targetcontainerrepository-repositoryname"></a>
The name of the container repository where the output container image is stored\. This name is prefixed by the repository location\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Service`  <a name="cfn-imagebuilder-distributionconfiguration-targetcontainerrepository-service"></a>
Specifies the service in which this image was registered\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ECR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)