# AWS::AppFlow::ConnectorProfile InforNexusConnectorProfileProperties<a name="aws-properties-appflow-connectorprofile-infornexusconnectorprofileproperties"></a>

 The `InforNexusConnectorProfileProperties` property type specifies the connector\-specific profile properties required by Infor Nexus\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-infornexusconnectorprofileproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-infornexusconnectorprofileproperties-syntax.json"></a>

```
{
  "[InstanceUrl](#cfn-appflow-connectorprofile-infornexusconnectorprofileproperties-instanceurl)" : String
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-infornexusconnectorprofileproperties-syntax.yaml"></a>

```
  [InstanceUrl](#cfn-appflow-connectorprofile-infornexusconnectorprofileproperties-instanceurl): String
```

## Properties<a name="aws-properties-appflow-connectorprofile-infornexusconnectorprofileproperties-properties"></a>

`InstanceUrl`  <a name="cfn-appflow-connectorprofile-infornexusconnectorprofileproperties-instanceurl"></a>
 The location of the Infor Nexus resource\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-connectorprofile-infornexusconnectorprofileproperties--seealso"></a>
+ [InforNexusConnectorProfileProperties](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_InforNexusConnectorProfileProperties.html) in the *Amazon AppFlow API Reference*\.

