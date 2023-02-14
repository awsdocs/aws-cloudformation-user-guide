# AWS::AppFlow::ConnectorProfile ConnectorProfileConfig<a name="aws-properties-appflow-connectorprofile-connectorprofileconfig"></a>

 Defines the connector\-specific configuration and credentials for the connector profile\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-connectorprofileconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-connectorprofileconfig-syntax.json"></a>

```
{
  "[ConnectorProfileCredentials](#cfn-appflow-connectorprofile-connectorprofileconfig-connectorprofilecredentials)" : ConnectorProfileCredentials,
  "[ConnectorProfileProperties](#cfn-appflow-connectorprofile-connectorprofileconfig-connectorprofileproperties)" : ConnectorProfileProperties
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-connectorprofileconfig-syntax.yaml"></a>

```
  [ConnectorProfileCredentials](#cfn-appflow-connectorprofile-connectorprofileconfig-connectorprofilecredentials): 
    ConnectorProfileCredentials
  [ConnectorProfileProperties](#cfn-appflow-connectorprofile-connectorprofileconfig-connectorprofileproperties): 
    ConnectorProfileProperties
```

## Properties<a name="aws-properties-appflow-connectorprofile-connectorprofileconfig-properties"></a>

`ConnectorProfileCredentials`  <a name="cfn-appflow-connectorprofile-connectorprofileconfig-connectorprofilecredentials"></a>
 The connector\-specific credentials required by each connector\.   
*Required*: Yes  
*Type*: [ConnectorProfileCredentials](aws-properties-appflow-connectorprofile-connectorprofilecredentials.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectorProfileProperties`  <a name="cfn-appflow-connectorprofile-connectorprofileconfig-connectorprofileproperties"></a>
 The connector\-specific properties of the profile configuration\.   
*Required*: No  
*Type*: [ConnectorProfileProperties](aws-properties-appflow-connectorprofile-connectorprofileproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-connectorprofile-connectorprofileconfig--seealso"></a>
+ [ConnectorProfileConfig](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_ConnectorProfileConfig.html) in the *Amazon AppFlow API Reference*\.

