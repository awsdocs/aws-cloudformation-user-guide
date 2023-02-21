# AWS::AppRunner::ObservabilityConfiguration TraceConfiguration<a name="aws-properties-apprunner-observabilityconfiguration-traceconfiguration"></a>

Describes the configuration of the tracing feature within an AWS App Runner observability configuration\.

## Syntax<a name="aws-properties-apprunner-observabilityconfiguration-traceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apprunner-observabilityconfiguration-traceconfiguration-syntax.json"></a>

```
{
  "[Vendor](#cfn-apprunner-observabilityconfiguration-traceconfiguration-vendor)" : String
}
```

### YAML<a name="aws-properties-apprunner-observabilityconfiguration-traceconfiguration-syntax.yaml"></a>

```
  [Vendor](#cfn-apprunner-observabilityconfiguration-traceconfiguration-vendor): String
```

## Properties<a name="aws-properties-apprunner-observabilityconfiguration-traceconfiguration-properties"></a>

`Vendor`  <a name="cfn-apprunner-observabilityconfiguration-traceconfiguration-vendor"></a>
The implementation provider chosen for tracing App Runner services\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `AWSXRAY`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)