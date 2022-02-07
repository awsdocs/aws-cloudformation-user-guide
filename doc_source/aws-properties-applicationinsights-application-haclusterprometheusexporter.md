# AWS::ApplicationInsights::Application HAClusterPrometheusExporter<a name="aws-properties-applicationinsights-application-haclusterprometheusexporter"></a>

The `AWS::ApplicationInsights::Application HAClusterPrometheusExporter` property type defines the HA cluster Prometheus Exporter settings\. For more information, see the [component configuration](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/component-config-sections.html#component-configuration-prometheus) in the CloudWatch Application Insights documentation\.

## Syntax<a name="aws-properties-applicationinsights-application-haclusterprometheusexporter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationinsights-application-haclusterprometheusexporter-syntax.json"></a>

```
{
  "[PrometheusPort](#cfn-applicationinsights-application-haclusterprometheusexporter-prometheusport)" : String
}
```

### YAML<a name="aws-properties-applicationinsights-application-haclusterprometheusexporter-syntax.yaml"></a>

```
  [PrometheusPort](#cfn-applicationinsights-application-haclusterprometheusexporter-prometheusport): String
```

## Properties<a name="aws-properties-applicationinsights-application-haclusterprometheusexporter-properties"></a>

`PrometheusPort`  <a name="cfn-applicationinsights-application-haclusterprometheusexporter-prometheusport"></a>
The target port to which Prometheus sends metrics\. If not specified, the default port 9668 is used\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)