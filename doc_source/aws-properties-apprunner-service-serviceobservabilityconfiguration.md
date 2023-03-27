# AWS::AppRunner::Service ServiceObservabilityConfiguration<a name="aws-properties-apprunner-service-serviceobservabilityconfiguration"></a>

Describes the observability configuration of an AWS App Runner service\. These are additional observability features, like tracing, that you choose to enable\. They're configured in a separate resource that you associate with your service\.

## Syntax<a name="aws-properties-apprunner-service-serviceobservabilityconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apprunner-service-serviceobservabilityconfiguration-syntax.json"></a>

```
{
  "[ObservabilityConfigurationArn](#cfn-apprunner-service-serviceobservabilityconfiguration-observabilityconfigurationarn)" : String,
  "[ObservabilityEnabled](#cfn-apprunner-service-serviceobservabilityconfiguration-observabilityenabled)" : Boolean
}
```

### YAML<a name="aws-properties-apprunner-service-serviceobservabilityconfiguration-syntax.yaml"></a>

```
  [ObservabilityConfigurationArn](#cfn-apprunner-service-serviceobservabilityconfiguration-observabilityconfigurationarn): String
  [ObservabilityEnabled](#cfn-apprunner-service-serviceobservabilityconfiguration-observabilityenabled): Boolean
```

## Properties<a name="aws-properties-apprunner-service-serviceobservabilityconfiguration-properties"></a>

`ObservabilityConfigurationArn`  <a name="cfn-apprunner-service-serviceobservabilityconfiguration-observabilityconfigurationarn"></a>
The Amazon Resource Name \(ARN\) of the observability configuration that is associated with the service\. Specified only when `ObservabilityEnabled` is `true`\.  
Specify an ARN with a name and a revision number to associate that revision\. For example: `arn:aws:apprunner:us-east-1:123456789012:observabilityconfiguration/xray-tracing/3`   
Specify just the name to associate the latest revision\. For example: `arn:aws:apprunner:us-east-1:123456789012:observabilityconfiguration/xray-tracing`   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1011`  
*Pattern*: `arn:aws(-[\w]+)*:[a-z0-9-\\.]{0,63}:[a-z0-9-\\.]{0,63}:[0-9]{12}:(\w|\/|-){1,1011}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObservabilityEnabled`  <a name="cfn-apprunner-service-serviceobservabilityconfiguration-observabilityenabled"></a>
When `true`, an observability configuration resource is associated with the service, and an `ObservabilityConfigurationArn` is specified\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)