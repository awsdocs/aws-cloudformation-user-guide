# AWS::Events::Connection BasicAuthParameters<a name="aws-properties-events-connection-basicauthparameters"></a>

Contains the Basic authorization parameters for the connection\.

## Syntax<a name="aws-properties-events-connection-basicauthparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-connection-basicauthparameters-syntax.json"></a>

```
{
  "[Password](#cfn-events-connection-basicauthparameters-password)" : String,
  "[Username](#cfn-events-connection-basicauthparameters-username)" : String
}
```

### YAML<a name="aws-properties-events-connection-basicauthparameters-syntax.yaml"></a>

```
  [Password](#cfn-events-connection-basicauthparameters-password): String
  [Username](#cfn-events-connection-basicauthparameters-username): String
```

## Properties<a name="aws-properties-events-connection-basicauthparameters-properties"></a>

`Password`  <a name="cfn-events-connection-basicauthparameters-password"></a>
The password associated with the user name to use for Basic authorization\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `^[ \t]*[^\x00-\x1F:\x7F]+([ \t]+[^\x00-\x1F:\x7F]+)*[ \t]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Username`  <a name="cfn-events-connection-basicauthparameters-username"></a>
The user name to use for Basic authorization\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `^[ \t]*[^\x00-\x1F:\x7F]+([ \t]+[^\x00-\x1F:\x7F]+)*[ \t]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)