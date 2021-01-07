# AWS::AppFlow::ConnectorProfile TrendmicroConnectorProfileCredentials<a name="aws-properties-appflow-connectorprofile-trendmicroconnectorprofilecredentials"></a>

 The `TrendmicroConnectorProfileCredentials` property type specifies the connector\-specific profile credentials required when using Trend Micro\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-trendmicroconnectorprofilecredentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-trendmicroconnectorprofilecredentials-syntax.json"></a>

```
{
  "[ApiSecretKey](#cfn-appflow-connectorprofile-trendmicroconnectorprofilecredentials-apisecretkey)" : String
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-trendmicroconnectorprofilecredentials-syntax.yaml"></a>

```
  [ApiSecretKey](#cfn-appflow-connectorprofile-trendmicroconnectorprofilecredentials-apisecretkey): String
```

## Properties<a name="aws-properties-appflow-connectorprofile-trendmicroconnectorprofilecredentials-properties"></a>

`ApiSecretKey`  <a name="cfn-appflow-connectorprofile-trendmicroconnectorprofilecredentials-apisecretkey"></a>
 The Secret Access Key portion of the credentials\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-connectorprofile-trendmicroconnectorprofilecredentials--seealso"></a>
+ [TrendmicroConnectorProfileCredentials](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_TrendmicroConnectorProfileCredentials.html) in the *Amazon AppFlow API Reference*\.

