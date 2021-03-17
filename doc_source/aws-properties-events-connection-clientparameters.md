# AWS::Events::Connection ClientParameters<a name="aws-properties-events-connection-clientparameters"></a>

Contains the client parameters for OAuth authorization\.

## Syntax<a name="aws-properties-events-connection-clientparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-connection-clientparameters-syntax.json"></a>

```
{
  "[ClientID](#cfn-events-connection-clientparameters-clientid)" : String,
  "[ClientSecret](#cfn-events-connection-clientparameters-clientsecret)" : String
}
```

### YAML<a name="aws-properties-events-connection-clientparameters-syntax.yaml"></a>

```
  [ClientID](#cfn-events-connection-clientparameters-clientid): String
  [ClientSecret](#cfn-events-connection-clientparameters-clientsecret): String
```

## Properties<a name="aws-properties-events-connection-clientparameters-properties"></a>

`ClientID`  <a name="cfn-events-connection-clientparameters-clientid"></a>
The client secret associated with the client ID to use for OAuth authorization for the connection\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientSecret`  <a name="cfn-events-connection-clientparameters-clientsecret"></a>
The client ID to use for OAuth authorization for the connection\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)