# AWS::AppFlow::Flow SourceConnectorProperties<a name="aws-properties-appflow-flow-sourceconnectorproperties"></a>

 Specifies the information that is required to query a particular connector\. 

## Syntax<a name="aws-properties-appflow-flow-sourceconnectorproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-sourceconnectorproperties-syntax.json"></a>

```
{
  "[Amplitude](#cfn-appflow-flow-sourceconnectorproperties-amplitude)" : AmplitudeSourceProperties,
  "[Datadog](#cfn-appflow-flow-sourceconnectorproperties-datadog)" : DatadogSourceProperties,
  "[Dynatrace](#cfn-appflow-flow-sourceconnectorproperties-dynatrace)" : DynatraceSourceProperties,
  "[GoogleAnalytics](#cfn-appflow-flow-sourceconnectorproperties-googleanalytics)" : GoogleAnalyticsSourceProperties,
  "[InforNexus](#cfn-appflow-flow-sourceconnectorproperties-infornexus)" : InforNexusSourceProperties,
  "[Marketo](#cfn-appflow-flow-sourceconnectorproperties-marketo)" : MarketoSourceProperties,
  "[S3](#cfn-appflow-flow-sourceconnectorproperties-s3)" : S3SourceProperties,
  "[Salesforce](#cfn-appflow-flow-sourceconnectorproperties-salesforce)" : SalesforceSourceProperties,
  "[ServiceNow](#cfn-appflow-flow-sourceconnectorproperties-servicenow)" : ServiceNowSourceProperties,
  "[Singular](#cfn-appflow-flow-sourceconnectorproperties-singular)" : SingularSourceProperties,
  "[Slack](#cfn-appflow-flow-sourceconnectorproperties-slack)" : SlackSourceProperties,
  "[Trendmicro](#cfn-appflow-flow-sourceconnectorproperties-trendmicro)" : TrendmicroSourceProperties,
  "[Veeva](#cfn-appflow-flow-sourceconnectorproperties-veeva)" : VeevaSourceProperties,
  "[Zendesk](#cfn-appflow-flow-sourceconnectorproperties-zendesk)" : ZendeskSourceProperties
}
```

### YAML<a name="aws-properties-appflow-flow-sourceconnectorproperties-syntax.yaml"></a>

```
  [Amplitude](#cfn-appflow-flow-sourceconnectorproperties-amplitude): 
    AmplitudeSourceProperties
  [Datadog](#cfn-appflow-flow-sourceconnectorproperties-datadog): 
    DatadogSourceProperties
  [Dynatrace](#cfn-appflow-flow-sourceconnectorproperties-dynatrace): 
    DynatraceSourceProperties
  [GoogleAnalytics](#cfn-appflow-flow-sourceconnectorproperties-googleanalytics): 
    GoogleAnalyticsSourceProperties
  [InforNexus](#cfn-appflow-flow-sourceconnectorproperties-infornexus): 
    InforNexusSourceProperties
  [Marketo](#cfn-appflow-flow-sourceconnectorproperties-marketo): 
    MarketoSourceProperties
  [S3](#cfn-appflow-flow-sourceconnectorproperties-s3): 
    S3SourceProperties
  [Salesforce](#cfn-appflow-flow-sourceconnectorproperties-salesforce): 
    SalesforceSourceProperties
  [ServiceNow](#cfn-appflow-flow-sourceconnectorproperties-servicenow): 
    ServiceNowSourceProperties
  [Singular](#cfn-appflow-flow-sourceconnectorproperties-singular): 
    SingularSourceProperties
  [Slack](#cfn-appflow-flow-sourceconnectorproperties-slack): 
    SlackSourceProperties
  [Trendmicro](#cfn-appflow-flow-sourceconnectorproperties-trendmicro): 
    TrendmicroSourceProperties
  [Veeva](#cfn-appflow-flow-sourceconnectorproperties-veeva): 
    VeevaSourceProperties
  [Zendesk](#cfn-appflow-flow-sourceconnectorproperties-zendesk): 
    ZendeskSourceProperties
```

## Properties<a name="aws-properties-appflow-flow-sourceconnectorproperties-properties"></a>

`Amplitude`  <a name="cfn-appflow-flow-sourceconnectorproperties-amplitude"></a>
 Specifies the information that is required for querying Amplitude\.   
*Required*: No  
*Type*: [AmplitudeSourceProperties](aws-properties-appflow-flow-amplitudesourceproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Datadog`  <a name="cfn-appflow-flow-sourceconnectorproperties-datadog"></a>
 Specifies the information that is required for querying Datadog\.   
*Required*: No  
*Type*: [DatadogSourceProperties](aws-properties-appflow-flow-datadogsourceproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Dynatrace`  <a name="cfn-appflow-flow-sourceconnectorproperties-dynatrace"></a>
 Specifies the information that is required for querying Dynatrace\.   
*Required*: No  
*Type*: [DynatraceSourceProperties](aws-properties-appflow-flow-dynatracesourceproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GoogleAnalytics`  <a name="cfn-appflow-flow-sourceconnectorproperties-googleanalytics"></a>
 Specifies the information that is required for querying Google Analytics\.   
*Required*: No  
*Type*: [GoogleAnalyticsSourceProperties](aws-properties-appflow-flow-googleanalyticssourceproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InforNexus`  <a name="cfn-appflow-flow-sourceconnectorproperties-infornexus"></a>
 Specifies the information that is required for querying Infor Nexus\.   
*Required*: No  
*Type*: [InforNexusSourceProperties](aws-properties-appflow-flow-infornexussourceproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Marketo`  <a name="cfn-appflow-flow-sourceconnectorproperties-marketo"></a>
 Specifies the information that is required for querying Marketo\.   
*Required*: No  
*Type*: [MarketoSourceProperties](aws-properties-appflow-flow-marketosourceproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3`  <a name="cfn-appflow-flow-sourceconnectorproperties-s3"></a>
 Specifies the information that is required for querying Amazon S3\.   
*Required*: No  
*Type*: [S3SourceProperties](aws-properties-appflow-flow-s3sourceproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Salesforce`  <a name="cfn-appflow-flow-sourceconnectorproperties-salesforce"></a>
 Specifies the information that is required for querying Salesforce\.   
*Required*: No  
*Type*: [SalesforceSourceProperties](aws-properties-appflow-flow-salesforcesourceproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceNow`  <a name="cfn-appflow-flow-sourceconnectorproperties-servicenow"></a>
 Specifies the information that is required for querying ServiceNow\.   
*Required*: No  
*Type*: [ServiceNowSourceProperties](aws-properties-appflow-flow-servicenowsourceproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Singular`  <a name="cfn-appflow-flow-sourceconnectorproperties-singular"></a>
 Specifies the information that is required for querying Singular\.   
*Required*: No  
*Type*: [SingularSourceProperties](aws-properties-appflow-flow-singularsourceproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Slack`  <a name="cfn-appflow-flow-sourceconnectorproperties-slack"></a>
 Specifies the information that is required for querying Slack\.   
*Required*: No  
*Type*: [SlackSourceProperties](aws-properties-appflow-flow-slacksourceproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Trendmicro`  <a name="cfn-appflow-flow-sourceconnectorproperties-trendmicro"></a>
 Specifies the information that is required for querying Trend Micro\.   
*Required*: No  
*Type*: [TrendmicroSourceProperties](aws-properties-appflow-flow-trendmicrosourceproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Veeva`  <a name="cfn-appflow-flow-sourceconnectorproperties-veeva"></a>
 Specifies the information that is required for querying Veeva\.   
*Required*: No  
*Type*: [VeevaSourceProperties](aws-properties-appflow-flow-veevasourceproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Zendesk`  <a name="cfn-appflow-flow-sourceconnectorproperties-zendesk"></a>
 Specifies the information that is required for querying Zendesk\.   
*Required*: No  
*Type*: [ZendeskSourceProperties](aws-properties-appflow-flow-zendesksourceproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-flow-sourceconnectorproperties--seealso"></a>
+ [SourceConnectorProperties](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_SourceConnectorProperties.html) in the *Amazon AppFlow API Reference*\.

