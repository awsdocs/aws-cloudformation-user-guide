# AWS::AppRunner::Service CodeConfigurationValues<a name="aws-properties-apprunner-service-codeconfigurationvalues"></a>

Describes the basic configuration needed for building and running an AWS App Runner service\. This type doesn't support the full set of possible configuration options\. Fur full configuration capabilities, use a `apprunner.yaml` file in the source code repository\.

## Syntax<a name="aws-properties-apprunner-service-codeconfigurationvalues-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apprunner-service-codeconfigurationvalues-syntax.json"></a>

```
{
  "[BuildCommand](#cfn-apprunner-service-codeconfigurationvalues-buildcommand)" : String,
  "[Port](#cfn-apprunner-service-codeconfigurationvalues-port)" : String,
  "[Runtime](#cfn-apprunner-service-codeconfigurationvalues-runtime)" : String,
  "[RuntimeEnvironmentVariables](#cfn-apprunner-service-codeconfigurationvalues-runtimeenvironmentvariables)" : [ KeyValuePair, ... ],
  "[StartCommand](#cfn-apprunner-service-codeconfigurationvalues-startcommand)" : String
}
```

### YAML<a name="aws-properties-apprunner-service-codeconfigurationvalues-syntax.yaml"></a>

```
  [BuildCommand](#cfn-apprunner-service-codeconfigurationvalues-buildcommand): String
  [Port](#cfn-apprunner-service-codeconfigurationvalues-port): String
  [Runtime](#cfn-apprunner-service-codeconfigurationvalues-runtime): String
  [RuntimeEnvironmentVariables](#cfn-apprunner-service-codeconfigurationvalues-runtimeenvironmentvariables): 
    - KeyValuePair
  [StartCommand](#cfn-apprunner-service-codeconfigurationvalues-startcommand): String
```

## Properties<a name="aws-properties-apprunner-service-codeconfigurationvalues-properties"></a>

`BuildCommand`  <a name="cfn-apprunner-service-codeconfigurationvalues-buildcommand"></a>
The command App Runner runs to build your application\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-apprunner-service-codeconfigurationvalues-port"></a>
The port that your application listens to in the container\.  
Default: `8080`   
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `51200`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Runtime`  <a name="cfn-apprunner-service-codeconfigurationvalues-runtime"></a>
A runtime environment type for building and running an App Runner service\. It represents a programming language runtime\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CORRETTO_11 | CORRETTO_8 | NODEJS_12 | NODEJS_14 | PYTHON_3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuntimeEnvironmentVariables`  <a name="cfn-apprunner-service-codeconfigurationvalues-runtimeenvironmentvariables"></a>
The environment variables that are available to your running App Runner service\. An array of key\-value pairs\. Keys with a prefix of `AWSAPPRUNNER` are reserved for system use and aren't valid\.  
*Required*: No  
*Type*: List of [KeyValuePair](aws-properties-apprunner-service-keyvaluepair.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartCommand`  <a name="cfn-apprunner-service-codeconfigurationvalues-startcommand"></a>
The command App Runner runs to start your application\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)