# AWS::AppFlow::ConnectorProfile AmplitudeConnectorProfileCredentials<a name="aws-properties-appflow-connectorprofile-amplitudeconnectorprofilecredentials"></a>

 The `AmplitudeConnectorProfileCredentials` property type specifies the connector\-specific credentials required when using Amplitude\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-amplitudeconnectorprofilecredentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-amplitudeconnectorprofilecredentials-syntax.json"></a>

```
{
  "[ApiKey](#cfn-appflow-connectorprofile-amplitudeconnectorprofilecredentials-apikey)" : String,
  "[SecretKey](#cfn-appflow-connectorprofile-amplitudeconnectorprofilecredentials-secretkey)" : String
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-amplitudeconnectorprofilecredentials-syntax.yaml"></a>

```
  [ApiKey](#cfn-appflow-connectorprofile-amplitudeconnectorprofilecredentials-apikey): String
  [SecretKey](#cfn-appflow-connectorprofile-amplitudeconnectorprofilecredentials-secretkey): String
```

## Properties<a name="aws-properties-appflow-connectorprofile-amplitudeconnectorprofilecredentials-properties"></a>

`ApiKey`  <a name="cfn-appflow-connectorprofile-amplitudeconnectorprofilecredentials-apikey"></a>
 A unique alphanumeric identifier used to authenticate a user, developer, or calling program to your API\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretKey`  <a name="cfn-appflow-connectorprofile-amplitudeconnectorprofilecredentials-secretkey"></a>
 The Secret Access Key portion of the credentials\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-connectorprofile-amplitudeconnectorprofilecredentials--seealso"></a>
+ [AmplitudeConnectorProfileCredentials](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_AmplitudeConnectorProfileCredentials.html) in the *Amazon AppFlow API Reference*\.

