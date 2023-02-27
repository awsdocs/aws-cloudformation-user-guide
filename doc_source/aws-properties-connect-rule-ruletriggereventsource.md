# AWS::Connect::Rule RuleTriggerEventSource<a name="aws-properties-connect-rule-ruletriggereventsource"></a>

The name of the event source\. 

## Syntax<a name="aws-properties-connect-rule-ruletriggereventsource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-rule-ruletriggereventsource-syntax.json"></a>

```
{
  "[EventSourceName](#cfn-connect-rule-ruletriggereventsource-eventsourcename)" : String,
  "[IntegrationAssociationArn](#cfn-connect-rule-ruletriggereventsource-integrationassociationarn)" : String
}
```

### YAML<a name="aws-properties-connect-rule-ruletriggereventsource-syntax.yaml"></a>

```
  [EventSourceName](#cfn-connect-rule-ruletriggereventsource-eventsourcename): String
  [IntegrationAssociationArn](#cfn-connect-rule-ruletriggereventsource-integrationassociationarn): String
```

## Properties<a name="aws-properties-connect-rule-ruletriggereventsource-properties"></a>

`EventSourceName`  <a name="cfn-connect-rule-ruletriggereventsource-eventsourcename"></a>
The name of the event source\.   
*Allowed values*: `OnPostCallAnalysisAvailable` \| `OnRealTimeCallAnalysisAvailable` \| `OnPostChatAnalysisAvailable` \| `OnZendeskTicketCreate` \| `OnZendeskTicketStatusUpdate` \| `OnSalesforceCaseCreate`  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IntegrationAssociationArn`  <a name="cfn-connect-rule-ruletriggereventsource-integrationassociationarn"></a>
 The Amazon Resource Name \(ARN\) for the integration association\. `IntegrationAssociationArn` is required if `TriggerEventSource` is one of the following values: `OnZendeskTicketCreate` \| `OnZendeskTicketStatusUpdate` \| `OnSalesforceCaseCreate`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)