# AWS::Events::Connection ClientParameters<a name="aws-properties-events-connection-clientparameters"></a>

Contains the OAuth authorization parameters to use for the connection\.

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
The client ID to use for OAuth authorization\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `^[ \t]*[^\x00-\x1F:\x7F]+([ \t]+[^\x00-\x1F:\x7F]+)*[ \t]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientSecret`  <a name="cfn-events-connection-clientparameters-clientsecret"></a>
The client secret assciated with the client ID to use for OAuth authorization\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `^[ \t]*[^\x00-\x1F:\x7F]+([ \t]+[^\x00-\x1F:\x7F]+)*[ \t]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)