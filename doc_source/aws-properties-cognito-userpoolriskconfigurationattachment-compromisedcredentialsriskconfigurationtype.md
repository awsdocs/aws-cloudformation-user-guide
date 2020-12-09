# AWS::Cognito::UserPoolRiskConfigurationAttachment CompromisedCredentialsRiskConfigurationType<a name="aws-properties-cognito-userpoolriskconfigurationattachment-compromisedcredentialsriskconfigurationtype"></a>

The compromised credentials risk configuration type\.

## Syntax<a name="aws-properties-cognito-userpoolriskconfigurationattachment-compromisedcredentialsriskconfigurationtype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpoolriskconfigurationattachment-compromisedcredentialsriskconfigurationtype-syntax.json"></a>

```
{
  "[Actions](#cfn-cognito-userpoolriskconfigurationattachment-compromisedcredentialsriskconfigurationtype-actions)" : CompromisedCredentialsActionsType,
  "[EventFilter](#cfn-cognito-userpoolriskconfigurationattachment-compromisedcredentialsriskconfigurationtype-eventfilter)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cognito-userpoolriskconfigurationattachment-compromisedcredentialsriskconfigurationtype-syntax.yaml"></a>

```
  [Actions](#cfn-cognito-userpoolriskconfigurationattachment-compromisedcredentialsriskconfigurationtype-actions): 
    CompromisedCredentialsActionsType
  [EventFilter](#cfn-cognito-userpoolriskconfigurationattachment-compromisedcredentialsriskconfigurationtype-eventfilter): 
    - String
```

## Properties<a name="aws-properties-cognito-userpoolriskconfigurationattachment-compromisedcredentialsriskconfigurationtype-properties"></a>

`Actions`  <a name="cfn-cognito-userpoolriskconfigurationattachment-compromisedcredentialsriskconfigurationtype-actions"></a>
The compromised credentials risk configuration actions\.  
*Required*: Yes  
*Type*: [CompromisedCredentialsActionsType](aws-properties-cognito-userpoolriskconfigurationattachment-compromisedcredentialsactionstype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EventFilter`  <a name="cfn-cognito-userpoolriskconfigurationattachment-compromisedcredentialsriskconfigurationtype-eventfilter"></a>
Perform the action for these events\. The default is to perform all events if no event filter is specified\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)