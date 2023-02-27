# AWS::AppFlow::ConnectorProfile ApiKeyCredentials<a name="aws-properties-appflow-connectorprofile-apikeycredentials"></a>

The API key credentials required for API key authentication\.

## Syntax<a name="aws-properties-appflow-connectorprofile-apikeycredentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-apikeycredentials-syntax.json"></a>

```
{
  "[ApiKey](#cfn-appflow-connectorprofile-apikeycredentials-apikey)" : String,
  "[ApiSecretKey](#cfn-appflow-connectorprofile-apikeycredentials-apisecretkey)" : String
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-apikeycredentials-syntax.yaml"></a>

```
  [ApiKey](#cfn-appflow-connectorprofile-apikeycredentials-apikey): String
  [ApiSecretKey](#cfn-appflow-connectorprofile-apikeycredentials-apisecretkey): String
```

## Properties<a name="aws-properties-appflow-connectorprofile-apikeycredentials-properties"></a>

`ApiKey`  <a name="cfn-appflow-connectorprofile-apikeycredentials-apikey"></a>
The API key required for API key authentication\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ApiSecretKey`  <a name="cfn-appflow-connectorprofile-apikeycredentials-apisecretkey"></a>
The API secret key required for API key authentication\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)