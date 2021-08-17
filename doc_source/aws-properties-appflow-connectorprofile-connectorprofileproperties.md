# AWS::AppFlow::ConnectorProfile ConnectorProfileProperties<a name="aws-properties-appflow-connectorprofile-connectorprofileproperties"></a>

 The `ConnectorProfileProperties` property type specifies the connector\-specific profile properties required by each connector\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-connectorprofileproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-connectorprofileproperties-syntax.json"></a>

```
{
  "[Datadog](#cfn-appflow-connectorprofile-connectorprofileproperties-datadog)" : DatadogConnectorProfileProperties,
  "[Dynatrace](#cfn-appflow-connectorprofile-connectorprofileproperties-dynatrace)" : DynatraceConnectorProfileProperties,
  "[InforNexus](#cfn-appflow-connectorprofile-connectorprofileproperties-infornexus)" : InforNexusConnectorProfileProperties,
  "[Marketo](#cfn-appflow-connectorprofile-connectorprofileproperties-marketo)" : MarketoConnectorProfileProperties,
  "[Redshift](#cfn-appflow-connectorprofile-connectorprofileproperties-redshift)" : RedshiftConnectorProfileProperties,
  "[Salesforce](#cfn-appflow-connectorprofile-connectorprofileproperties-salesforce)" : SalesforceConnectorProfileProperties,
  "[ServiceNow](#cfn-appflow-connectorprofile-connectorprofileproperties-servicenow)" : ServiceNowConnectorProfileProperties,
  "[Slack](#cfn-appflow-connectorprofile-connectorprofileproperties-slack)" : SlackConnectorProfileProperties,
  "[Snowflake](#cfn-appflow-connectorprofile-connectorprofileproperties-snowflake)" : SnowflakeConnectorProfileProperties,
  "[Veeva](#cfn-appflow-connectorprofile-connectorprofileproperties-veeva)" : VeevaConnectorProfileProperties,
  "[Zendesk](#cfn-appflow-connectorprofile-connectorprofileproperties-zendesk)" : ZendeskConnectorProfileProperties
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-connectorprofileproperties-syntax.yaml"></a>

```
  [Datadog](#cfn-appflow-connectorprofile-connectorprofileproperties-datadog): 
    DatadogConnectorProfileProperties
  [Dynatrace](#cfn-appflow-connectorprofile-connectorprofileproperties-dynatrace): 
    DynatraceConnectorProfileProperties
  [InforNexus](#cfn-appflow-connectorprofile-connectorprofileproperties-infornexus): 
    InforNexusConnectorProfileProperties
  [Marketo](#cfn-appflow-connectorprofile-connectorprofileproperties-marketo): 
    MarketoConnectorProfileProperties
  [Redshift](#cfn-appflow-connectorprofile-connectorprofileproperties-redshift): 
    RedshiftConnectorProfileProperties
  [Salesforce](#cfn-appflow-connectorprofile-connectorprofileproperties-salesforce): 
    SalesforceConnectorProfileProperties
  [ServiceNow](#cfn-appflow-connectorprofile-connectorprofileproperties-servicenow): 
    ServiceNowConnectorProfileProperties
  [Slack](#cfn-appflow-connectorprofile-connectorprofileproperties-slack): 
    SlackConnectorProfileProperties
  [Snowflake](#cfn-appflow-connectorprofile-connectorprofileproperties-snowflake): 
    SnowflakeConnectorProfileProperties
  [Veeva](#cfn-appflow-connectorprofile-connectorprofileproperties-veeva): 
    VeevaConnectorProfileProperties
  [Zendesk](#cfn-appflow-connectorprofile-connectorprofileproperties-zendesk): 
    ZendeskConnectorProfileProperties
```

## Properties<a name="aws-properties-appflow-connectorprofile-connectorprofileproperties-properties"></a>

`Datadog`  <a name="cfn-appflow-connectorprofile-connectorprofileproperties-datadog"></a>
 The connector\-specific properties required by Datadog\.   
*Required*: No  
*Type*: [DatadogConnectorProfileProperties](aws-properties-appflow-connectorprofile-datadogconnectorprofileproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Dynatrace`  <a name="cfn-appflow-connectorprofile-connectorprofileproperties-dynatrace"></a>
 The connector\-specific properties required by Dynatrace\.   
*Required*: No  
*Type*: [DynatraceConnectorProfileProperties](aws-properties-appflow-connectorprofile-dynatraceconnectorprofileproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InforNexus`  <a name="cfn-appflow-connectorprofile-connectorprofileproperties-infornexus"></a>
 The connector\-specific properties required by Infor Nexus\.   
*Required*: No  
*Type*: [InforNexusConnectorProfileProperties](aws-properties-appflow-connectorprofile-infornexusconnectorprofileproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Marketo`  <a name="cfn-appflow-connectorprofile-connectorprofileproperties-marketo"></a>
 The connector\-specific properties required by Marketo\.   
*Required*: No  
*Type*: [MarketoConnectorProfileProperties](aws-properties-appflow-connectorprofile-marketoconnectorprofileproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Redshift`  <a name="cfn-appflow-connectorprofile-connectorprofileproperties-redshift"></a>
 The connector\-specific properties required by Amazon Redshift\.   
*Required*: No  
*Type*: [RedshiftConnectorProfileProperties](aws-properties-appflow-connectorprofile-redshiftconnectorprofileproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Salesforce`  <a name="cfn-appflow-connectorprofile-connectorprofileproperties-salesforce"></a>
 The connector\-specific properties required by Salesforce\.   
*Required*: No  
*Type*: [SalesforceConnectorProfileProperties](aws-properties-appflow-connectorprofile-salesforceconnectorprofileproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceNow`  <a name="cfn-appflow-connectorprofile-connectorprofileproperties-servicenow"></a>
 The connector\-specific properties required by serviceNow\.   
*Required*: No  
*Type*: [ServiceNowConnectorProfileProperties](aws-properties-appflow-connectorprofile-servicenowconnectorprofileproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Slack`  <a name="cfn-appflow-connectorprofile-connectorprofileproperties-slack"></a>
 The connector\-specific properties required by Slack\.   
*Required*: No  
*Type*: [SlackConnectorProfileProperties](aws-properties-appflow-connectorprofile-slackconnectorprofileproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Snowflake`  <a name="cfn-appflow-connectorprofile-connectorprofileproperties-snowflake"></a>
 The connector\-specific properties required by Snowflake\.   
*Required*: No  
*Type*: [SnowflakeConnectorProfileProperties](aws-properties-appflow-connectorprofile-snowflakeconnectorprofileproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Veeva`  <a name="cfn-appflow-connectorprofile-connectorprofileproperties-veeva"></a>
 The connector\-specific properties required by Veeva\.   
*Required*: No  
*Type*: [VeevaConnectorProfileProperties](aws-properties-appflow-connectorprofile-veevaconnectorprofileproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Zendesk`  <a name="cfn-appflow-connectorprofile-connectorprofileproperties-zendesk"></a>
 The connector\-specific properties required by Zendesk\.   
*Required*: No  
*Type*: [ZendeskConnectorProfileProperties](aws-properties-appflow-connectorprofile-zendeskconnectorprofileproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-connectorprofile-connectorprofileproperties--seealso"></a>
+ [ConnectorProfileProperties](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_ConnectorProfileProperties.html) in the *Amazon AppFlow API Reference*\.

