# AWS::ApplicationInsights::Application HANAPrometheusExporter<a name="aws-properties-applicationinsights-application-hanaprometheusexporter"></a>

The `AWS::ApplicationInsights::Application HANAPrometheusExporter` property type defines the HANA DB Prometheus Exporter settings\. For more information, see the [component configuration](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/component-config-sections.html#component-configuration-prometheus) in the CloudWatch Application Insights documentation\.

## Syntax<a name="aws-properties-applicationinsights-application-hanaprometheusexporter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-applicationinsights-application-hanaprometheusexporter-syntax.json"></a>

```
{
  "[AgreeToInstallHANADBClient](#cfn-applicationinsights-application-hanaprometheusexporter-agreetoinstallhanadbclient)" : Boolean,
  "[HANAPort](#cfn-applicationinsights-application-hanaprometheusexporter-hanaport)" : String,
  "[HANASecretName](#cfn-applicationinsights-application-hanaprometheusexporter-hanasecretname)" : String,
  "[HANASID](#cfn-applicationinsights-application-hanaprometheusexporter-hanasid)" : String,
  "[PrometheusPort](#cfn-applicationinsights-application-hanaprometheusexporter-prometheusport)" : String
}
```

### YAML<a name="aws-properties-applicationinsights-application-hanaprometheusexporter-syntax.yaml"></a>

```
  [AgreeToInstallHANADBClient](#cfn-applicationinsights-application-hanaprometheusexporter-agreetoinstallhanadbclient): Boolean
  [HANAPort](#cfn-applicationinsights-application-hanaprometheusexporter-hanaport): String
  [HANASecretName](#cfn-applicationinsights-application-hanaprometheusexporter-hanasecretname): String
  [HANASID](#cfn-applicationinsights-application-hanaprometheusexporter-hanasid): String
  [PrometheusPort](#cfn-applicationinsights-application-hanaprometheusexporter-prometheusport): String
```

## Properties<a name="aws-properties-applicationinsights-application-hanaprometheusexporter-properties"></a>

`AgreeToInstallHANADBClient`  <a name="cfn-applicationinsights-application-hanaprometheusexporter-agreetoinstallhanadbclient"></a>
Designates whether you agree to install the HANA DB client\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HANAPort`  <a name="cfn-applicationinsights-application-hanaprometheusexporter-hanaport"></a>
The HANA database port by which the exporter will query HANA metrics\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HANASecretName`  <a name="cfn-applicationinsights-application-hanaprometheusexporter-hanasecretname"></a>
The AWS Secrets Manager secret that stores HANA monitoring user credentials\. The HANA Prometheus exporter uses these credentials to connect to the database and query HANA metrics\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HANASID`  <a name="cfn-applicationinsights-application-hanaprometheusexporter-hanasid"></a>
The three\-character SAP system ID \(SID\) of the SAP HANA system\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrometheusPort`  <a name="cfn-applicationinsights-application-hanaprometheusexporter-prometheusport"></a>
The target port to which Prometheus sends metrics\. If not specified, the default port 9668 is used\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)