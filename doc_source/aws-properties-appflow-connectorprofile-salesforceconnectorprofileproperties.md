# AWS::AppFlow::ConnectorProfile SalesforceConnectorProfileProperties<a name="aws-properties-appflow-connectorprofile-salesforceconnectorprofileproperties"></a>

 The `SalesforceConnectorProfileProperties` property type specifies the connector\-specific profile properties required when using Salesforce\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-salesforceconnectorprofileproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-salesforceconnectorprofileproperties-syntax.json"></a>

```
{
  "[InstanceUrl](#cfn-appflow-connectorprofile-salesforceconnectorprofileproperties-instanceurl)" : String,
  "[isSandboxEnvironment](#cfn-appflow-connectorprofile-salesforceconnectorprofileproperties-issandboxenvironment)" : Boolean
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-salesforceconnectorprofileproperties-syntax.yaml"></a>

```
  [InstanceUrl](#cfn-appflow-connectorprofile-salesforceconnectorprofileproperties-instanceurl): String
  [isSandboxEnvironment](#cfn-appflow-connectorprofile-salesforceconnectorprofileproperties-issandboxenvironment): Boolean
```

## Properties<a name="aws-properties-appflow-connectorprofile-salesforceconnectorprofileproperties-properties"></a>

`InstanceUrl`  <a name="cfn-appflow-connectorprofile-salesforceconnectorprofileproperties-instanceurl"></a>
 The location of the Salesforce resource\.   
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`isSandboxEnvironment`  <a name="cfn-appflow-connectorprofile-salesforceconnectorprofileproperties-issandboxenvironment"></a>
 Indicates whether the connector profile applies to a sandbox or production environment\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-connectorprofile-salesforceconnectorprofileproperties--seealso"></a>
+ [SalesforceConnectorProfileProperties](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_SalesforceConnectorProfileProperties.html) in the *Amazon AppFlow API Reference*\.

