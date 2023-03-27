# AWS::SSMIncidents::ResponsePlan<a name="aws-resource-ssmincidents-responseplan"></a>

The `AWS::SSMIncidents::ResponsePlan` resource specifies the details of the response plan that are used when creating an incident\.

## Syntax<a name="aws-resource-ssmincidents-responseplan-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssmincidents-responseplan-syntax.json"></a>

```
{
  "Type" : "AWS::SSMIncidents::ResponsePlan",
  "Properties" : {
      "[Actions](#cfn-ssmincidents-responseplan-actions)" : [ Action, ... ],
      "[ChatChannel](#cfn-ssmincidents-responseplan-chatchannel)" : ChatChannel,
      "[DisplayName](#cfn-ssmincidents-responseplan-displayname)" : String,
      "[Engagements](#cfn-ssmincidents-responseplan-engagements)" : [ String, ... ],
      "[IncidentTemplate](#cfn-ssmincidents-responseplan-incidenttemplate)" : IncidentTemplate,
      "[Integrations](#cfn-ssmincidents-responseplan-integrations)" : [ Integration, ... ],
      "[Name](#cfn-ssmincidents-responseplan-name)" : String,
      "[Tags](#cfn-ssmincidents-responseplan-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ssmincidents-responseplan-syntax.yaml"></a>

```
Type: AWS::SSMIncidents::ResponsePlan
Properties: 
  [Actions](#cfn-ssmincidents-responseplan-actions): 
    - Action
  [ChatChannel](#cfn-ssmincidents-responseplan-chatchannel): 
    ChatChannel
  [DisplayName](#cfn-ssmincidents-responseplan-displayname): String
  [Engagements](#cfn-ssmincidents-responseplan-engagements): 
    - String
  [IncidentTemplate](#cfn-ssmincidents-responseplan-incidenttemplate): 
    IncidentTemplate
  [Integrations](#cfn-ssmincidents-responseplan-integrations): 
    - Integration
  [Name](#cfn-ssmincidents-responseplan-name): String
  [Tags](#cfn-ssmincidents-responseplan-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ssmincidents-responseplan-properties"></a>

`Actions`  <a name="cfn-ssmincidents-responseplan-actions"></a>
The actions that the response plan starts at the beginning of an incident\.  
*Required*: No  
*Type*: List of [Action](aws-properties-ssmincidents-responseplan-action.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChatChannel`  <a name="cfn-ssmincidents-responseplan-chatchannel"></a>
The AWS Chatbot chat channel used for collaboration during an incident\.  
*Required*: No  
*Type*: [ChatChannel](aws-properties-ssmincidents-responseplan-chatchannel.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisplayName`  <a name="cfn-ssmincidents-responseplan-displayname"></a>
The human readable name of the response plan\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Engagements`  <a name="cfn-ssmincidents-responseplan-engagements"></a>
The Amazon Resource Name \(ARN\) for the contacts and escalation plans that the response plan engages during an incident\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncidentTemplate`  <a name="cfn-ssmincidents-responseplan-incidenttemplate"></a>
Details used to create an incident when using this response plan\.  
*Required*: Yes  
*Type*: [IncidentTemplate](aws-properties-ssmincidents-responseplan-incidenttemplate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Integrations`  <a name="cfn-ssmincidents-responseplan-integrations"></a>
Information about third\-party services integrated into the response plan\.  
*Required*: No  
*Type*: List of [Integration](aws-properties-ssmincidents-responseplan-integration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-ssmincidents-responseplan-name"></a>
The name of the response plan\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `200`  
*Pattern*: `^[a-zA-Z0-9-_]*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ssmincidents-responseplan-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)