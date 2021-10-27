# AWS::ECR::Repository ImageScanningConfiguration<a name="aws-properties-ecr-repository-imagescanningconfiguration"></a>

The image scanning configuration for a repository\.

## Syntax<a name="aws-properties-ecr-repository-imagescanningconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecr-repository-imagescanningconfiguration-syntax.json"></a>

```
{
  "[ScanOnPush](#cfn-ecr-repository-imagescanningconfiguration-scanonpush)" : Boolean
}
```

### YAML<a name="aws-properties-ecr-repository-imagescanningconfiguration-syntax.yaml"></a>

```
  [ScanOnPush](#cfn-ecr-repository-imagescanningconfiguration-scanonpush): Boolean
```

## Properties<a name="aws-properties-ecr-repository-imagescanningconfiguration-properties"></a>

`ScanOnPush`  <a name="cfn-ecr-repository-imagescanningconfiguration-scanonpush"></a>
The setting that determines whether images are scanned after being pushed to a repository\. If set to `true`, images will be scanned after being pushed\. If this parameter is not specified, it will default to `false` and images will not be scanned unless a scan is manually started\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)