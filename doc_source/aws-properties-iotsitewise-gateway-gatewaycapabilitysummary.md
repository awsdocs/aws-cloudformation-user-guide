# AWS::IoTSiteWise::Gateway GatewayCapabilitySummary<a name="aws-properties-iotsitewise-gateway-gatewaycapabilitysummary"></a>

Contains a summary of a gateway capability configuration\.

## Syntax<a name="aws-properties-iotsitewise-gateway-gatewaycapabilitysummary-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotsitewise-gateway-gatewaycapabilitysummary-syntax.json"></a>

```
{
  "[CapabilityConfiguration](#cfn-iotsitewise-gateway-gatewaycapabilitysummary-capabilityconfiguration)" : String,
  "[CapabilityNamespace](#cfn-iotsitewise-gateway-gatewaycapabilitysummary-capabilitynamespace)" : String
}
```

### YAML<a name="aws-properties-iotsitewise-gateway-gatewaycapabilitysummary-syntax.yaml"></a>

```
  [CapabilityConfiguration](#cfn-iotsitewise-gateway-gatewaycapabilitysummary-capabilityconfiguration): String
  [CapabilityNamespace](#cfn-iotsitewise-gateway-gatewaycapabilitysummary-capabilitynamespace): String
```

## Properties<a name="aws-properties-iotsitewise-gateway-gatewaycapabilitysummary-properties"></a>

`CapabilityConfiguration`  <a name="cfn-iotsitewise-gateway-gatewaycapabilitysummary-capabilityconfiguration"></a>
The JSON document that defines the configuration for the gateway capability\. For more information, see [Configuring data sources \(CLI\)](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/configure-sources.html#configure-source-cli) in the *AWS IoT SiteWise User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CapabilityNamespace`  <a name="cfn-iotsitewise-gateway-gatewaycapabilitysummary-capabilitynamespace"></a>
The namespace of the capability configuration\. For example, if you configure OPC\-UA sources from the AWS IoT SiteWise console, your OPC\-UA capability configuration has the namespace `iotsitewise:opcuacollector:version`, where `version` is a number such as `1`\.  
The maximum length is 512 characters with the pattern `^[a-zA-Z]+:[a-zA-Z]+:[0-9]+$`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)