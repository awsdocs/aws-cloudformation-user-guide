# AWS::Cognito::UserPoolRiskConfigurationAttachment CompromisedCredentialsActionsType<a name="aws-properties-cognito-userpoolriskconfigurationattachment-compromisedcredentialsactionstype"></a>

The compromised credentials actions type

## Syntax<a name="aws-properties-cognito-userpoolriskconfigurationattachment-compromisedcredentialsactionstype-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cognito-userpoolriskconfigurationattachment-compromisedcredentialsactionstype-syntax.json"></a>

```
{
  "[EventAction](#cfn-cognito-userpoolriskconfigurationattachment-compromisedcredentialsactionstype-eventaction)" : String
}
```

### YAML<a name="aws-properties-cognito-userpoolriskconfigurationattachment-compromisedcredentialsactionstype-syntax.yaml"></a>

```
  [EventAction](#cfn-cognito-userpoolriskconfigurationattachment-compromisedcredentialsactionstype-eventaction): String
```

## Properties<a name="aws-properties-cognito-userpoolriskconfigurationattachment-compromisedcredentialsactionstype-properties"></a>

`EventAction`  <a name="cfn-cognito-userpoolriskconfigurationattachment-compromisedcredentialsactionstype-eventaction"></a>
The event action\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `BLOCK | NO_ACTION`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)