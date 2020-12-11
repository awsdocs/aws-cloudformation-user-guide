# AWS::AppFlow::ConnectorProfile DynatraceConnectorProfileCredentials<a name="aws-properties-appflow-connectorprofile-dynatraceconnectorprofilecredentials"></a>

 The `DynatraceConnectorProfileCredentials` property type specifies the connector\-specific profile credentials required by Dynatrace\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-dynatraceconnectorprofilecredentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-dynatraceconnectorprofilecredentials-syntax.json"></a>

```
{
  "[ApiToken](#cfn-appflow-connectorprofile-dynatraceconnectorprofilecredentials-apitoken)" : String
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-dynatraceconnectorprofilecredentials-syntax.yaml"></a>

```
  [ApiToken](#cfn-appflow-connectorprofile-dynatraceconnectorprofilecredentials-apitoken): String
```

## Properties<a name="aws-properties-appflow-connectorprofile-dynatraceconnectorprofilecredentials-properties"></a>

`ApiToken`  <a name="cfn-appflow-connectorprofile-dynatraceconnectorprofilecredentials-apitoken"></a>
 The API tokens used by Dynatrace API to authenticate various API calls\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-connectorprofile-dynatraceconnectorprofilecredentials--seealso"></a>
+ [DynatraceConnectorProfileCredentials](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_DynatraceConnectorProfileCredentials.html) in the *Amazon AppFlow API Reference*\.

