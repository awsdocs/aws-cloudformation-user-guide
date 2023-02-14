# AWS::AppRunner::Service ImageConfiguration<a name="aws-properties-apprunner-service-imageconfiguration"></a>

Describes the configuration that AWS App Runner uses to run an App Runner service using an image pulled from a source image repository\.

## Syntax<a name="aws-properties-apprunner-service-imageconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apprunner-service-imageconfiguration-syntax.json"></a>

```
{
  "[Port](#cfn-apprunner-service-imageconfiguration-port)" : String,
  "[RuntimeEnvironmentVariables](#cfn-apprunner-service-imageconfiguration-runtimeenvironmentvariables)" : [ KeyValuePair, ... ],
  "[StartCommand](#cfn-apprunner-service-imageconfiguration-startcommand)" : String
}
```

### YAML<a name="aws-properties-apprunner-service-imageconfiguration-syntax.yaml"></a>

```
  [Port](#cfn-apprunner-service-imageconfiguration-port): String
  [RuntimeEnvironmentVariables](#cfn-apprunner-service-imageconfiguration-runtimeenvironmentvariables): 
    - KeyValuePair
  [StartCommand](#cfn-apprunner-service-imageconfiguration-startcommand): String
```

## Properties<a name="aws-properties-apprunner-service-imageconfiguration-properties"></a>

`Port`  <a name="cfn-apprunner-service-imageconfiguration-port"></a>
The port that your application listens to in the container\.  
Default: `8080`   
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `51200`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuntimeEnvironmentVariables`  <a name="cfn-apprunner-service-imageconfiguration-runtimeenvironmentvariables"></a>
Environment variables that are available to your running App Runner service\. An array of key\-value pairs\. Keys with a prefix of `AWSAPPRUNNER` are reserved for system use and aren't valid\.  
*Required*: No  
*Type*: List of [KeyValuePair](aws-properties-apprunner-service-keyvaluepair.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartCommand`  <a name="cfn-apprunner-service-imageconfiguration-startcommand"></a>
An optional command that App Runner runs to start the application in the source image\. If specified, this command overrides the Docker image’s default start command\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `51200`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)