# AWS::AppRunner::ObservabilityConfiguration<a name="aws-resource-apprunner-observabilityconfiguration"></a>

The `AWS::AppRunner::ObservabilityConfiguration` resource is an AWS App Runner resource type that specifies an App Runner observability configuration\.

App Runner requires this resource when you specify App Runner services and you want to enable non\-default observability features\. You can share an observability configuration across multiple services\.

Create multiple revisions of a configuration by specifying this resource multiple times using the same `ObservabilityConfigurationName`\. App Runner creates multiple resources with incremental `ObservabilityConfigurationRevision` values\. When you specify a service and configure an observability configuration resource, the service uses the latest active revision of the observability configuration by default\. You can optionally configure the service to use a specific revision\.

The observability configuration resource is designed to configure multiple features \(currently one feature, tracing\)\. This resource takes optional parameters that describe the configuration of these features \(currently one parameter, `TraceConfiguration`\)\. If you don't specify a feature parameter, App Runner doesn't enable the feature\.

## Syntax<a name="aws-resource-apprunner-observabilityconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apprunner-observabilityconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::AppRunner::ObservabilityConfiguration",
  "Properties" : {
      "[ObservabilityConfigurationName](#cfn-apprunner-observabilityconfiguration-observabilityconfigurationname)" : String,
      "[Tags](#cfn-apprunner-observabilityconfiguration-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TraceConfiguration](#cfn-apprunner-observabilityconfiguration-traceconfiguration)" : TraceConfiguration
    }
}
```

### YAML<a name="aws-resource-apprunner-observabilityconfiguration-syntax.yaml"></a>

```
Type: AWS::AppRunner::ObservabilityConfiguration
Properties: 
  [ObservabilityConfigurationName](#cfn-apprunner-observabilityconfiguration-observabilityconfigurationname): String
  [Tags](#cfn-apprunner-observabilityconfiguration-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TraceConfiguration](#cfn-apprunner-observabilityconfiguration-traceconfiguration): 
    TraceConfiguration
```

## Properties<a name="aws-resource-apprunner-observabilityconfiguration-properties"></a>

`ObservabilityConfigurationName`  <a name="cfn-apprunner-observabilityconfiguration-observabilityconfigurationname"></a>
A name for the observability configuration\. When you use it for the first time in an AWS Region, App Runner creates revision number `1` of this name\. When you use the same name in subsequent calls, App Runner creates incremental revisions of the configuration\.  
The name `DefaultConfiguration` is reserved\. You can't use it to create a new observability configuration, and you can't create a revision of it\.  
When you want to use your own observability configuration for your App Runner service, *create a configuration with a different name*, and then provide it when you create or update your service\.
If you don't specify a name, AWS CloudFormation generates a name for your observability configuration\.  
*Required*: No  
*Type*: String  
*Minimum*: `4`  
*Maximum*: `32`  
*Pattern*: `[A-Za-z0-9][A-Za-z0-9\-_]{3,31}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-apprunner-observabilityconfiguration-tags"></a>
A list of metadata items that you can associate with your observability configuration resource\. A tag is a key\-value pair\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TraceConfiguration`  <a name="cfn-apprunner-observabilityconfiguration-traceconfiguration"></a>
The configuration of the tracing feature within this observability configuration\. If you don't specify it, App Runner doesn't enable tracing\.  
*Required*: No  
*Type*: [TraceConfiguration](aws-properties-apprunner-observabilityconfiguration-traceconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-apprunner-observabilityconfiguration-return-values"></a>

### Ref<a name="aws-resource-apprunner-observabilityconfiguration-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-apprunner-observabilityconfiguration-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-apprunner-observabilityconfiguration-return-values-fn--getatt-fn--getatt"></a>

`Latest`  <a name="Latest-fn::getatt"></a>
It's set to `true` for the configuration with the highest `Revision` among all configurations that share the same `ObservabilityConfigurationName`\. It's set to `false` otherwise\.

`ObservabilityConfigurationArn`  <a name="ObservabilityConfigurationArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of this observability configuration\.

`ObservabilityConfigurationRevision`  <a name="ObservabilityConfigurationRevision-fn::getatt"></a>
The revision of this observability configuration\. It's unique among all the active configurations \(`"Status": "ACTIVE"`\) that share the same `ObservabilityConfigurationName`\.

## Examples<a name="aws-resource-apprunner-observabilityconfiguration--examples"></a>

### Observability configuration to enable tracing<a name="aws-resource-apprunner-observabilityconfiguration--examples--Observability_configuration_to_enable_tracing"></a>

This example illustrates creating an observability configuration that enables tracing using AWS X\-Ray\.

#### JSON<a name="aws-resource-apprunner-observabilityconfiguration--examples--Observability_configuration_to_enable_tracing--json"></a>

```
{
  "Type": "AWS::AppRunner::ObservabilityConfiguration",
  "Properties": {
    "ObservabilityConfigurationName": "xray-tracing",
    "TraceConfiguration": {
      "Vendor": "AWSXRAY"
    }
  }
}
```

#### YAML<a name="aws-resource-apprunner-observabilityconfiguration--examples--Observability_configuration_to_enable_tracing--yaml"></a>

```
Type: AWS::AppRunner::ObservabilityConfiguration
Properties:
  ObservabilityConfigurationName: xray-tracing
  TraceConfiguration:
    Vendor: AWSXRAY
```

## See also<a name="aws-resource-apprunner-observabilityconfiguration--seealso"></a>
+ [Tracing for your App Runner application with X\-Ray](https://docs.aws.amazon.com/apprunner/latest/dg/monitor-xray.html) in the *AWS App Runner Developer Guide*