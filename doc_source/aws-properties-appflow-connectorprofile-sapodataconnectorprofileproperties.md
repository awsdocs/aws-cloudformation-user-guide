# AWS::AppFlow::ConnectorProfile SAPODataConnectorProfileProperties<a name="aws-properties-appflow-connectorprofile-sapodataconnectorprofileproperties"></a>

 The connector\-specific profile properties required when using SAPOData\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-sapodataconnectorprofileproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-sapodataconnectorprofileproperties-syntax.json"></a>

```
{
  "[ApplicationHostUrl](#cfn-appflow-connectorprofile-sapodataconnectorprofileproperties-applicationhosturl)" : String,
  "[ApplicationServicePath](#cfn-appflow-connectorprofile-sapodataconnectorprofileproperties-applicationservicepath)" : String,
  "[ClientNumber](#cfn-appflow-connectorprofile-sapodataconnectorprofileproperties-clientnumber)" : String,
  "[LogonLanguage](#cfn-appflow-connectorprofile-sapodataconnectorprofileproperties-logonlanguage)" : String,
  "[OAuthProperties](#cfn-appflow-connectorprofile-sapodataconnectorprofileproperties-oauthproperties)" : OAuthProperties,
  "[PortNumber](#cfn-appflow-connectorprofile-sapodataconnectorprofileproperties-portnumber)" : Integer,
  "[PrivateLinkServiceName](#cfn-appflow-connectorprofile-sapodataconnectorprofileproperties-privatelinkservicename)" : String
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-sapodataconnectorprofileproperties-syntax.yaml"></a>

```
  [ApplicationHostUrl](#cfn-appflow-connectorprofile-sapodataconnectorprofileproperties-applicationhosturl): String
  [ApplicationServicePath](#cfn-appflow-connectorprofile-sapodataconnectorprofileproperties-applicationservicepath): String
  [ClientNumber](#cfn-appflow-connectorprofile-sapodataconnectorprofileproperties-clientnumber): String
  [LogonLanguage](#cfn-appflow-connectorprofile-sapodataconnectorprofileproperties-logonlanguage): String
  [OAuthProperties](#cfn-appflow-connectorprofile-sapodataconnectorprofileproperties-oauthproperties): 
    OAuthProperties
  [PortNumber](#cfn-appflow-connectorprofile-sapodataconnectorprofileproperties-portnumber): Integer
  [PrivateLinkServiceName](#cfn-appflow-connectorprofile-sapodataconnectorprofileproperties-privatelinkservicename): String
```

## Properties<a name="aws-properties-appflow-connectorprofile-sapodataconnectorprofileproperties-properties"></a>

`ApplicationHostUrl`  <a name="cfn-appflow-connectorprofile-sapodataconnectorprofileproperties-applicationhosturl"></a>
 The location of the SAPOData resource\.   
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `^(https?)://[-a-zA-Z0-9+&@#/%?=~_|!:,.;]*[-a-zA-Z0-9+&@#/%=~_|]`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ApplicationServicePath`  <a name="cfn-appflow-connectorprofile-sapodataconnectorprofileproperties-applicationservicepath"></a>
 The application path to catalog service\.   
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientNumber`  <a name="cfn-appflow-connectorprofile-sapodataconnectorprofileproperties-clientnumber"></a>
 The client number for the client creating the connection\.   
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `3`  
*Pattern*: `^\d{3}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogonLanguage`  <a name="cfn-appflow-connectorprofile-sapodataconnectorprofileproperties-logonlanguage"></a>
 The logon language of SAPOData instance\.   
*Required*: No  
*Type*: String  
*Maximum*: `2`  
*Pattern*: `^[a-zA-Z0-9_]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OAuthProperties`  <a name="cfn-appflow-connectorprofile-sapodataconnectorprofileproperties-oauthproperties"></a>
 The SAPOData OAuth properties required for OAuth type authentication\.   
*Required*: No  
*Type*: [OAuthProperties](aws-properties-appflow-connectorprofile-oauthproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PortNumber`  <a name="cfn-appflow-connectorprofile-sapodataconnectorprofileproperties-portnumber"></a>
 The port number of the SAPOData instance\.   
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrivateLinkServiceName`  <a name="cfn-appflow-connectorprofile-sapodataconnectorprofileproperties-privatelinkservicename"></a>
 The SAPOData Private Link service name to be used for private data transfers\.   
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `^$|com.amazonaws.vpce.[\w/!:@#.\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)