# AWS::AppFlow::ConnectorProfile ConnectorProfileCredentials<a name="aws-properties-appflow-connectorprofile-connectorprofilecredentials"></a>

 The `ConnectorProfileCredentials` property type specifies the connector\-specific credentials required by a given connector\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-connectorprofilecredentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-connectorprofilecredentials-syntax.json"></a>

```
{
  "[Amplitude](#cfn-appflow-connectorprofile-connectorprofilecredentials-amplitude)" : AmplitudeConnectorProfileCredentials,
  "[Datadog](#cfn-appflow-connectorprofile-connectorprofilecredentials-datadog)" : DatadogConnectorProfileCredentials,
  "[Dynatrace](#cfn-appflow-connectorprofile-connectorprofilecredentials-dynatrace)" : DynatraceConnectorProfileCredentials,
  "[GoogleAnalytics](#cfn-appflow-connectorprofile-connectorprofilecredentials-googleanalytics)" : GoogleAnalyticsConnectorProfileCredentials,
  "[InforNexus](#cfn-appflow-connectorprofile-connectorprofilecredentials-infornexus)" : InforNexusConnectorProfileCredentials,
  "[Marketo](#cfn-appflow-connectorprofile-connectorprofilecredentials-marketo)" : MarketoConnectorProfileCredentials,
  "[Redshift](#cfn-appflow-connectorprofile-connectorprofilecredentials-redshift)" : RedshiftConnectorProfileCredentials,
  "[Salesforce](#cfn-appflow-connectorprofile-connectorprofilecredentials-salesforce)" : SalesforceConnectorProfileCredentials,
  "[ServiceNow](#cfn-appflow-connectorprofile-connectorprofilecredentials-servicenow)" : ServiceNowConnectorProfileCredentials,
  "[Singular](#cfn-appflow-connectorprofile-connectorprofilecredentials-singular)" : SingularConnectorProfileCredentials,
  "[Slack](#cfn-appflow-connectorprofile-connectorprofilecredentials-slack)" : SlackConnectorProfileCredentials,
  "[Snowflake](#cfn-appflow-connectorprofile-connectorprofilecredentials-snowflake)" : SnowflakeConnectorProfileCredentials,
  "[Trendmicro](#cfn-appflow-connectorprofile-connectorprofilecredentials-trendmicro)" : TrendmicroConnectorProfileCredentials,
  "[Veeva](#cfn-appflow-connectorprofile-connectorprofilecredentials-veeva)" : VeevaConnectorProfileCredentials,
  "[Zendesk](#cfn-appflow-connectorprofile-connectorprofilecredentials-zendesk)" : ZendeskConnectorProfileCredentials
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-connectorprofilecredentials-syntax.yaml"></a>

```
  [Amplitude](#cfn-appflow-connectorprofile-connectorprofilecredentials-amplitude): 
    AmplitudeConnectorProfileCredentials
  [Datadog](#cfn-appflow-connectorprofile-connectorprofilecredentials-datadog): 
    DatadogConnectorProfileCredentials
  [Dynatrace](#cfn-appflow-connectorprofile-connectorprofilecredentials-dynatrace): 
    DynatraceConnectorProfileCredentials
  [GoogleAnalytics](#cfn-appflow-connectorprofile-connectorprofilecredentials-googleanalytics): 
    GoogleAnalyticsConnectorProfileCredentials
  [InforNexus](#cfn-appflow-connectorprofile-connectorprofilecredentials-infornexus): 
    InforNexusConnectorProfileCredentials
  [Marketo](#cfn-appflow-connectorprofile-connectorprofilecredentials-marketo): 
    MarketoConnectorProfileCredentials
  [Redshift](#cfn-appflow-connectorprofile-connectorprofilecredentials-redshift): 
    RedshiftConnectorProfileCredentials
  [Salesforce](#cfn-appflow-connectorprofile-connectorprofilecredentials-salesforce): 
    SalesforceConnectorProfileCredentials
  [ServiceNow](#cfn-appflow-connectorprofile-connectorprofilecredentials-servicenow): 
    ServiceNowConnectorProfileCredentials
  [Singular](#cfn-appflow-connectorprofile-connectorprofilecredentials-singular): 
    SingularConnectorProfileCredentials
  [Slack](#cfn-appflow-connectorprofile-connectorprofilecredentials-slack): 
    SlackConnectorProfileCredentials
  [Snowflake](#cfn-appflow-connectorprofile-connectorprofilecredentials-snowflake): 
    SnowflakeConnectorProfileCredentials
  [Trendmicro](#cfn-appflow-connectorprofile-connectorprofilecredentials-trendmicro): 
    TrendmicroConnectorProfileCredentials
  [Veeva](#cfn-appflow-connectorprofile-connectorprofilecredentials-veeva): 
    VeevaConnectorProfileCredentials
  [Zendesk](#cfn-appflow-connectorprofile-connectorprofilecredentials-zendesk): 
    ZendeskConnectorProfileCredentials
```

## Properties<a name="aws-properties-appflow-connectorprofile-connectorprofilecredentials-properties"></a>

`Amplitude`  <a name="cfn-appflow-connectorprofile-connectorprofilecredentials-amplitude"></a>
 The connector\-specific credentials required when using Amplitude\.   
*Required*: No  
*Type*: [AmplitudeConnectorProfileCredentials](aws-properties-appflow-connectorprofile-amplitudeconnectorprofilecredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Datadog`  <a name="cfn-appflow-connectorprofile-connectorprofilecredentials-datadog"></a>
 The connector\-specific credentials required when using Datadog\.   
*Required*: No  
*Type*: [DatadogConnectorProfileCredentials](aws-properties-appflow-connectorprofile-datadogconnectorprofilecredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Dynatrace`  <a name="cfn-appflow-connectorprofile-connectorprofilecredentials-dynatrace"></a>
 The connector\-specific credentials required when using Dynatrace\.   
*Required*: No  
*Type*: [DynatraceConnectorProfileCredentials](aws-properties-appflow-connectorprofile-dynatraceconnectorprofilecredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GoogleAnalytics`  <a name="cfn-appflow-connectorprofile-connectorprofilecredentials-googleanalytics"></a>
 The connector\-specific credentials required when using Google Analytics\.   
*Required*: No  
*Type*: [GoogleAnalyticsConnectorProfileCredentials](aws-properties-appflow-connectorprofile-googleanalyticsconnectorprofilecredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InforNexus`  <a name="cfn-appflow-connectorprofile-connectorprofilecredentials-infornexus"></a>
 The connector\-specific credentials required when using Infor Nexus\.   
*Required*: No  
*Type*: [InforNexusConnectorProfileCredentials](aws-properties-appflow-connectorprofile-infornexusconnectorprofilecredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Marketo`  <a name="cfn-appflow-connectorprofile-connectorprofilecredentials-marketo"></a>
 The connector\-specific credentials required when using Marketo\.   
*Required*: No  
*Type*: [MarketoConnectorProfileCredentials](aws-properties-appflow-connectorprofile-marketoconnectorprofilecredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Redshift`  <a name="cfn-appflow-connectorprofile-connectorprofilecredentials-redshift"></a>
 The connector\-specific credentials required when using Amazon Redshift\.   
*Required*: No  
*Type*: [RedshiftConnectorProfileCredentials](aws-properties-appflow-connectorprofile-redshiftconnectorprofilecredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Salesforce`  <a name="cfn-appflow-connectorprofile-connectorprofilecredentials-salesforce"></a>
 The connector\-specific credentials required when using Salesforce\.   
*Required*: No  
*Type*: [SalesforceConnectorProfileCredentials](aws-properties-appflow-connectorprofile-salesforceconnectorprofilecredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceNow`  <a name="cfn-appflow-connectorprofile-connectorprofilecredentials-servicenow"></a>
 The connector\-specific credentials required when using ServiceNow\.   
*Required*: No  
*Type*: [ServiceNowConnectorProfileCredentials](aws-properties-appflow-connectorprofile-servicenowconnectorprofilecredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Singular`  <a name="cfn-appflow-connectorprofile-connectorprofilecredentials-singular"></a>
 The connector\-specific credentials required when using Singular\.   
*Required*: No  
*Type*: [SingularConnectorProfileCredentials](aws-properties-appflow-connectorprofile-singularconnectorprofilecredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Slack`  <a name="cfn-appflow-connectorprofile-connectorprofilecredentials-slack"></a>
 The connector\-specific credentials required when using Slack\.   
*Required*: No  
*Type*: [SlackConnectorProfileCredentials](aws-properties-appflow-connectorprofile-slackconnectorprofilecredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Snowflake`  <a name="cfn-appflow-connectorprofile-connectorprofilecredentials-snowflake"></a>
 The connector\-specific credentials required when using Snowflake\.   
*Required*: No  
*Type*: [SnowflakeConnectorProfileCredentials](aws-properties-appflow-connectorprofile-snowflakeconnectorprofilecredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Trendmicro`  <a name="cfn-appflow-connectorprofile-connectorprofilecredentials-trendmicro"></a>
 The connector\-specific credentials required when using Trend Micro\.   
*Required*: No  
*Type*: [TrendmicroConnectorProfileCredentials](aws-properties-appflow-connectorprofile-trendmicroconnectorprofilecredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Veeva`  <a name="cfn-appflow-connectorprofile-connectorprofilecredentials-veeva"></a>
 The connector\-specific credentials required when using Veeva\.   
*Required*: No  
*Type*: [VeevaConnectorProfileCredentials](aws-properties-appflow-connectorprofile-veevaconnectorprofilecredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Zendesk`  <a name="cfn-appflow-connectorprofile-connectorprofilecredentials-zendesk"></a>
 The connector\-specific credentials required when using Zendesk\.   
*Required*: No  
*Type*: [ZendeskConnectorProfileCredentials](aws-properties-appflow-connectorprofile-zendeskconnectorprofilecredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-connectorprofile-connectorprofilecredentials--seealso"></a>
+ [ConnectorProfileCredentials](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_ConnectorProfileCredentials.html) in the *Amazon AppFlow API Reference*\.

