# AWS::AppFlow::ConnectorProfile CustomConnectorProfileProperties<a name="aws-properties-appflow-connectorprofile-customconnectorprofileproperties"></a>

The profile properties required by the custom connector\.

## Syntax<a name="aws-properties-appflow-connectorprofile-customconnectorprofileproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-customconnectorprofileproperties-syntax.json"></a>

```
{
  "[OAuth2Properties](#cfn-appflow-connectorprofile-customconnectorprofileproperties-oauth2properties)" : OAuth2Properties,
  "[ProfileProperties](#cfn-appflow-connectorprofile-customconnectorprofileproperties-profileproperties)" : {Key : Value, ...}
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-customconnectorprofileproperties-syntax.yaml"></a>

```
  [OAuth2Properties](#cfn-appflow-connectorprofile-customconnectorprofileproperties-oauth2properties): 
    OAuth2Properties
  [ProfileProperties](#cfn-appflow-connectorprofile-customconnectorprofileproperties-profileproperties): 
    Key : Value
```

## Properties<a name="aws-properties-appflow-connectorprofile-customconnectorprofileproperties-properties"></a>

`OAuth2Properties`  <a name="cfn-appflow-connectorprofile-customconnectorprofileproperties-oauth2properties"></a>
The OAuth 2\.0 properties required for OAuth 2\.0 authentication\.  
*Required*: No  
*Type*: [OAuth2Properties](aws-properties-appflow-connectorprofile-oauth2properties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProfileProperties`  <a name="cfn-appflow-connectorprofile-customconnectorprofileproperties-profileproperties"></a>
A map of properties that are required to create a profile for the custom connector\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)