# AWS::AppFlow::ConnectorProfile SalesforceConnectorProfileProperties<a name="aws-properties-appflow-connectorprofile-salesforceconnectorprofileproperties"></a>

 The connector\-specific profile properties required when using Salesforce\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-salesforceconnectorprofileproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-salesforceconnectorprofileproperties-syntax.json"></a>

```
{
  "[InstanceUrl](#cfn-appflow-connectorprofile-salesforceconnectorprofileproperties-instanceurl)" : String,
  "[isSandboxEnvironment](#cfn-appflow-connectorprofile-salesforceconnectorprofileproperties-issandboxenvironment)" : Boolean,
  "[usePrivateLinkForMetadataAndAuthorization](#cfn-appflow-connectorprofile-salesforceconnectorprofileproperties-useprivatelinkformetadataandauthorization)" : Boolean
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-salesforceconnectorprofileproperties-syntax.yaml"></a>

```
  [InstanceUrl](#cfn-appflow-connectorprofile-salesforceconnectorprofileproperties-instanceurl): String
  [isSandboxEnvironment](#cfn-appflow-connectorprofile-salesforceconnectorprofileproperties-issandboxenvironment): Boolean
  [usePrivateLinkForMetadataAndAuthorization](#cfn-appflow-connectorprofile-salesforceconnectorprofileproperties-useprivatelinkformetadataandauthorization): Boolean
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

`usePrivateLinkForMetadataAndAuthorization`  <a name="cfn-appflow-connectorprofile-salesforceconnectorprofileproperties-useprivatelinkformetadataandauthorization"></a>
If the connection mode for the connector profile is private, this parameter sets whether Amazon AppFlow uses the private network to send metadata and authorization calls to Salesforce\. Amazon AppFlow sends private calls through AWS PrivateLink\. These calls travel through AWS infrastructure without being exposed to the public internet\.  
Set either of the following values:    
true  
Amazon AppFlow sends all calls to Salesforce over the private network\.  
These private calls are:  
+ Calls to get metadata about your Salesforce records\. This metadata describes your Salesforce objects and their fields\.
+ Calls to get or refresh access tokens that allow Amazon AppFlow to access your Salesforce records\.
+ Calls to transfer your Salesforce records as part of a flow run\.  
false  
The default value\. Amazon AppFlow sends some calls to Salesforce privately and other calls over the public internet\.  
The public calls are:   
+ Calls to get metadata about your Salesforce records\.
+ Calls to get or refresh access tokens\.
The private calls are:  
+ Calls to transfer your Salesforce records as part of a flow run\.
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-connectorprofile-salesforceconnectorprofileproperties--seealso"></a>
+ [SalesforceConnectorProfileProperties](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_SalesforceConnectorProfileProperties.html) in the *Amazon AppFlow API Reference*\.

