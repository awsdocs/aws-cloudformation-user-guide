# AWS::AppFlow::ConnectorProfile ServiceNowConnectorProfileCredentials<a name="aws-properties-appflow-connectorprofile-servicenowconnectorprofilecredentials"></a>

 The `ServiceNowConnectorProfileCredentials` property type specifies the connector\-specific profile credentials required when using ServiceNow\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-servicenowconnectorprofilecredentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-servicenowconnectorprofilecredentials-syntax.json"></a>

```
{
  "[Password](#cfn-appflow-connectorprofile-servicenowconnectorprofilecredentials-password)" : String,
  "[Username](#cfn-appflow-connectorprofile-servicenowconnectorprofilecredentials-username)" : String
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-servicenowconnectorprofilecredentials-syntax.yaml"></a>

```
  [Password](#cfn-appflow-connectorprofile-servicenowconnectorprofilecredentials-password): String
  [Username](#cfn-appflow-connectorprofile-servicenowconnectorprofilecredentials-username): String
```

## Properties<a name="aws-properties-appflow-connectorprofile-servicenowconnectorprofilecredentials-properties"></a>

`Password`  <a name="cfn-appflow-connectorprofile-servicenowconnectorprofilecredentials-password"></a>
 The password that corresponds to the user name\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Username`  <a name="cfn-appflow-connectorprofile-servicenowconnectorprofilecredentials-username"></a>
 The name of the user\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-connectorprofile-servicenowconnectorprofilecredentials--seealso"></a>
+ [ServiceNowConnectorProfileCredentials](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_ServiceNowConnectorProfileCredentials.html) in the *Amazon AppFlow API Reference*\.

