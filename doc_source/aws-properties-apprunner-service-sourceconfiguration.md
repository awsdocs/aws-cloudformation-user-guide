# AWS::AppRunner::Service SourceConfiguration<a name="aws-properties-apprunner-service-sourceconfiguration"></a>

Describes the source deployed to an AWS App Runner service\. It can be a code or an image repository\.

## Syntax<a name="aws-properties-apprunner-service-sourceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apprunner-service-sourceconfiguration-syntax.json"></a>

```
{
  "[AuthenticationConfiguration](#cfn-apprunner-service-sourceconfiguration-authenticationconfiguration)" : AuthenticationConfiguration,
  "[AutoDeploymentsEnabled](#cfn-apprunner-service-sourceconfiguration-autodeploymentsenabled)" : Boolean,
  "[CodeRepository](#cfn-apprunner-service-sourceconfiguration-coderepository)" : CodeRepository,
  "[ImageRepository](#cfn-apprunner-service-sourceconfiguration-imagerepository)" : ImageRepository
}
```

### YAML<a name="aws-properties-apprunner-service-sourceconfiguration-syntax.yaml"></a>

```
  [AuthenticationConfiguration](#cfn-apprunner-service-sourceconfiguration-authenticationconfiguration): 
    AuthenticationConfiguration
  [AutoDeploymentsEnabled](#cfn-apprunner-service-sourceconfiguration-autodeploymentsenabled): Boolean
  [CodeRepository](#cfn-apprunner-service-sourceconfiguration-coderepository): 
    CodeRepository
  [ImageRepository](#cfn-apprunner-service-sourceconfiguration-imagerepository): 
    ImageRepository
```

## Properties<a name="aws-properties-apprunner-service-sourceconfiguration-properties"></a>

`AuthenticationConfiguration`  <a name="cfn-apprunner-service-sourceconfiguration-authenticationconfiguration"></a>
Describes the resources that are needed to authenticate access to some source repositories\.  
*Required*: No  
*Type*: [AuthenticationConfiguration](aws-properties-apprunner-service-authenticationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutoDeploymentsEnabled`  <a name="cfn-apprunner-service-sourceconfiguration-autodeploymentsenabled"></a>
If `true`, continuous integration from the source repository is enabled for the App Runner service\. Each repository change \(including any source code commit or new image version\) starts a deployment\.  
Default: App Runner sets to `false` for a source image that uses an ECR Public repository or an ECR repository that's in an AWS account other than the one that the service is in\. App Runner sets to `true` in all other cases \(which currently include a source code repository or a source image using a same\-account ECR repository\)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CodeRepository`  <a name="cfn-apprunner-service-sourceconfiguration-coderepository"></a>
The description of a source code repository\.  
You must provide either this member or `ImageRepository` \(but not both\)\.  
*Required*: No  
*Type*: [CodeRepository](aws-properties-apprunner-service-coderepository.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageRepository`  <a name="cfn-apprunner-service-sourceconfiguration-imagerepository"></a>
The description of a source image repository\.  
You must provide either this member or `CodeRepository` \(but not both\)\.  
*Required*: No  
*Type*: [ImageRepository](aws-properties-apprunner-service-imagerepository.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)