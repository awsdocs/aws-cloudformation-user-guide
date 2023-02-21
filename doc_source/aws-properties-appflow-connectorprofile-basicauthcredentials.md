# AWS::AppFlow::ConnectorProfile BasicAuthCredentials<a name="aws-properties-appflow-connectorprofile-basicauthcredentials"></a>

 The basic auth credentials required for basic authentication\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-basicauthcredentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-basicauthcredentials-syntax.json"></a>

```
{
  "[Password](#cfn-appflow-connectorprofile-basicauthcredentials-password)" : String,
  "[Username](#cfn-appflow-connectorprofile-basicauthcredentials-username)" : String
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-basicauthcredentials-syntax.yaml"></a>

```
  [Password](#cfn-appflow-connectorprofile-basicauthcredentials-password): String
  [Username](#cfn-appflow-connectorprofile-basicauthcredentials-username): String
```

## Properties<a name="aws-properties-appflow-connectorprofile-basicauthcredentials-properties"></a>

`Password`  <a name="cfn-appflow-connectorprofile-basicauthcredentials-password"></a>
 The password to use to connect to a resource\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Username`  <a name="cfn-appflow-connectorprofile-basicauthcredentials-username"></a>
 The username to use to connect to a resource\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)