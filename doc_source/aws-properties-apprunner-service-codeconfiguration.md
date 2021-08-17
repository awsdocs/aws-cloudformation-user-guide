# AWS::AppRunner::Service CodeConfiguration<a name="aws-properties-apprunner-service-codeconfiguration"></a>

Describes the configuration that AWS App Runner uses to build and run an App Runner service from a source code repository\.

## Syntax<a name="aws-properties-apprunner-service-codeconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apprunner-service-codeconfiguration-syntax.json"></a>

```
{
  "[CodeConfigurationValues](#cfn-apprunner-service-codeconfiguration-codeconfigurationvalues)" : CodeConfigurationValues,
  "[ConfigurationSource](#cfn-apprunner-service-codeconfiguration-configurationsource)" : String
}
```

### YAML<a name="aws-properties-apprunner-service-codeconfiguration-syntax.yaml"></a>

```
  [CodeConfigurationValues](#cfn-apprunner-service-codeconfiguration-codeconfigurationvalues): 
    CodeConfigurationValues
  [ConfigurationSource](#cfn-apprunner-service-codeconfiguration-configurationsource): String
```

## Properties<a name="aws-properties-apprunner-service-codeconfiguration-properties"></a>

`CodeConfigurationValues`  <a name="cfn-apprunner-service-codeconfiguration-codeconfigurationvalues"></a>
The basic configuration for building and running the App Runner service\. Use it to quickly launch an App Runner service without providing a `apprunner.yaml` file in the source code repository \(or ignoring the file if it exists\)\.  
*Required*: No  
*Type*: [CodeConfigurationValues](aws-properties-apprunner-service-codeconfigurationvalues.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConfigurationSource`  <a name="cfn-apprunner-service-codeconfiguration-configurationsource"></a>
The source of the App Runner configuration\. Values are interpreted as follows:  
+  `REPOSITORY` – App Runner reads configuration values from the `apprunner.yaml` file in the source code repository and ignores `CodeConfigurationValues`\.
+  `API` – App Runner uses configuration values provided in `CodeConfigurationValues` and ignores the `apprunner.yaml` file in the source code repository\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `API | REPOSITORY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)