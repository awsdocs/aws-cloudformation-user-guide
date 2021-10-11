# AWS::AppRunner::Service ImageRepository<a name="aws-properties-apprunner-service-imagerepository"></a>

Describes a source image repository\.

## Syntax<a name="aws-properties-apprunner-service-imagerepository-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apprunner-service-imagerepository-syntax.json"></a>

```
{
  "[ImageConfiguration](#cfn-apprunner-service-imagerepository-imageconfiguration)" : ImageConfiguration,
  "[ImageIdentifier](#cfn-apprunner-service-imagerepository-imageidentifier)" : String,
  "[ImageRepositoryType](#cfn-apprunner-service-imagerepository-imagerepositorytype)" : String
}
```

### YAML<a name="aws-properties-apprunner-service-imagerepository-syntax.yaml"></a>

```
  [ImageConfiguration](#cfn-apprunner-service-imagerepository-imageconfiguration): 
    ImageConfiguration
  [ImageIdentifier](#cfn-apprunner-service-imagerepository-imageidentifier): String
  [ImageRepositoryType](#cfn-apprunner-service-imagerepository-imagerepositorytype): String
```

## Properties<a name="aws-properties-apprunner-service-imagerepository-properties"></a>

`ImageConfiguration`  <a name="cfn-apprunner-service-imagerepository-imageconfiguration"></a>
Configuration for running the identified image\.  
*Required*: No  
*Type*: [ImageConfiguration](aws-properties-apprunner-service-imageconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageIdentifier`  <a name="cfn-apprunner-service-imagerepository-imageidentifier"></a>
The identifier of an image\.  
For an image in Amazon Elastic Container Registry \(Amazon ECR\), this is an image name\. For the image name format, see [Pulling an image](https://docs.aws.amazon.com/AmazonECR/latest/userguide/docker-pull-ecr-image.html) in the *Amazon ECR User Guide*\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `([0-9]{12}.dkr.ecr.[a-z\-]+-[0-9]{1}.amazonaws.com\/((?:[a-z0-9]+(?:[._-][a-z0-9]+)*\/)*[a-z0-9]+(?:[._-][a-z0-9]+)*)(:([\w\d+\-=._:\/@])+|@([\w\d\:]+))?)|(^public\.ecr\.aws\/.+\/((?:[a-z0-9]+(?:[._-][a-z0-9]+)*\/)*[a-z0-9]+(?:[._-][a-z0-9]+)*)(:([\w\d+\-=._:\/@])+|@([\w\d\:]+))?)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageRepositoryType`  <a name="cfn-apprunner-service-imagerepository-imagerepositorytype"></a>
The type of the image repository\. This reflects the repository provider and whether the repository is private or public\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ECR | ECR_PUBLIC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)