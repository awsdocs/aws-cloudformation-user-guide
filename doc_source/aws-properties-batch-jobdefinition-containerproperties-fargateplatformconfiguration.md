# AWS::Batch::JobDefinition FargatePlatformConfiguration<a name="aws-properties-batch-jobdefinition-containerproperties-fargateplatformconfiguration"></a>

The platform configuration for jobs running on Fargate resources\. Jobs running on EC2 resources must not specify this parameter\.

## Syntax<a name="aws-properties-batch-jobdefinition-containerproperties-fargateplatformconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-containerproperties-fargateplatformconfiguration-syntax.json"></a>

```
{
  "[PlatformVersion](#cfn-batch-jobdefinition-containerproperties-fargateplatformconfiguration-platformversion)" : String
}
```

### YAML<a name="aws-properties-batch-jobdefinition-containerproperties-fargateplatformconfiguration-syntax.yaml"></a>

```
  [PlatformVersion](#cfn-batch-jobdefinition-containerproperties-fargateplatformconfiguration-platformversion): String
```

## Properties<a name="aws-properties-batch-jobdefinition-containerproperties-fargateplatformconfiguration-properties"></a>

`PlatformVersion`  <a name="cfn-batch-jobdefinition-containerproperties-fargateplatformconfiguration-platformversion"></a>
The AWS Fargate platform version on which the jobs are running\. A platform version is specified only for jobs running on Fargate resources\. If one isn't specified, the `LATEST` platform version is used by default\. This will use a recent, approved version of the AWS Fargate platform for compute resources\. For more information, see [AWS Fargate platform versions](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/platform_versions.html) in the *Amazon Elastic Container Service Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)