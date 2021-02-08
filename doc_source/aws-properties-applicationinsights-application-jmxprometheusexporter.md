# AWS::ApplicationInsights::Application JMXPrometheusExporter<a name="aws-properties-applicationinsights-application-jmxprometheusexporter"></a>

The `AWS::ApplicationInsights::Application JMXPrometheusExporter` property type defines the JMXPrometheus Exporter configuration\. For more information, see the [component configuration](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/component-config-sections.html#component-configuration-prometheus) in the CloudWatch Application Insights documentation\.

## Syntax<a name="aws-properties-applicationinsights-application-jmxprometheusexporter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationinsights-application-jmxprometheusexporter-syntax.json"></a>

```
{
  "[HostPort](#cfn-applicationinsights-application-jmxprometheusexporter-hostport)" : String,
  "[JMXURL](#cfn-applicationinsights-application-jmxprometheusexporter-jmxurl)" : String,
  "[PrometheusPort](#cfn-applicationinsights-application-jmxprometheusexporter-prometheusport)" : String
}
```

### YAML<a name="aws-properties-applicationinsights-application-jmxprometheusexporter-syntax.yaml"></a>

```
  [HostPort](#cfn-applicationinsights-application-jmxprometheusexporter-hostport): String
  [JMXURL](#cfn-applicationinsights-application-jmxprometheusexporter-jmxurl): String
  [PrometheusPort](#cfn-applicationinsights-application-jmxprometheusexporter-prometheusport): String
```

## Properties<a name="aws-properties-applicationinsights-application-jmxprometheusexporter-properties"></a>

`HostPort`  <a name="cfn-applicationinsights-application-jmxprometheusexporter-hostport"></a>
The host and port to connect to through remote JMX\. Only one of `jmxURL` and `hostPort` can be specified\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JMXURL`  <a name="cfn-applicationinsights-application-jmxprometheusexporter-jmxurl"></a>
The complete JMX URL to connect to\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrometheusPort`  <a name="cfn-applicationinsights-application-jmxprometheusexporter-prometheusport"></a>
The target port to send Prometheus metrics to\. If not specified, the default port `9404` is used\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)