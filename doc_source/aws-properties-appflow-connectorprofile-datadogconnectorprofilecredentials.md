# AWS::AppFlow::ConnectorProfile DatadogConnectorProfileCredentials<a name="aws-properties-appflow-connectorprofile-datadogconnectorprofilecredentials"></a>

 The `DatadogConnectorProfileCredentials` property type specifies the connector\-specific credentials required by Datadog\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-datadogconnectorprofilecredentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-datadogconnectorprofilecredentials-syntax.json"></a>

```
{
  "[ApiKey](#cfn-appflow-connectorprofile-datadogconnectorprofilecredentials-apikey)" : String,
  "[ApplicationKey](#cfn-appflow-connectorprofile-datadogconnectorprofilecredentials-applicationkey)" : String
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-datadogconnectorprofilecredentials-syntax.yaml"></a>

```
  [ApiKey](#cfn-appflow-connectorprofile-datadogconnectorprofilecredentials-apikey): String
  [ApplicationKey](#cfn-appflow-connectorprofile-datadogconnectorprofilecredentials-applicationkey): String
```

## Properties<a name="aws-properties-appflow-connectorprofile-datadogconnectorprofilecredentials-properties"></a>

`ApiKey`  <a name="cfn-appflow-connectorprofile-datadogconnectorprofilecredentials-apikey"></a>
 A unique alphanumeric identifier used to authenticate a user, developer, or calling program to your API\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ApplicationKey`  <a name="cfn-appflow-connectorprofile-datadogconnectorprofilecredentials-applicationkey"></a>
 Application keys, in conjunction with your API key, give you full access to Datadog’s programmatic API\. Application keys are associated with the user account that created them\. The application key is used to log all requests made to the API\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-connectorprofile-datadogconnectorprofilecredentials--seealso"></a>
+ [DatadogConnectorProfileCredentials](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_DatadogConnectorProfileCredentials.html) in the *Amazon AppFlow API Reference*\.

