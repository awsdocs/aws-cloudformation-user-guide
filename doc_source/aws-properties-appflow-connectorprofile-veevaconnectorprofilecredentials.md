# AWS::AppFlow::ConnectorProfile VeevaConnectorProfileCredentials<a name="aws-properties-appflow-connectorprofile-veevaconnectorprofilecredentials"></a>

 The `VeevaConnectorProfileCredentials` property type specifies the connector\-specific profile credentials required when using Veeva\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-veevaconnectorprofilecredentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-veevaconnectorprofilecredentials-syntax.json"></a>

```
{
  "[Password](#cfn-appflow-connectorprofile-veevaconnectorprofilecredentials-password)" : String,
  "[Username](#cfn-appflow-connectorprofile-veevaconnectorprofilecredentials-username)" : String
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-veevaconnectorprofilecredentials-syntax.yaml"></a>

```
  [Password](#cfn-appflow-connectorprofile-veevaconnectorprofilecredentials-password): String
  [Username](#cfn-appflow-connectorprofile-veevaconnectorprofilecredentials-username): String
```

## Properties<a name="aws-properties-appflow-connectorprofile-veevaconnectorprofilecredentials-properties"></a>

`Password`  <a name="cfn-appflow-connectorprofile-veevaconnectorprofilecredentials-password"></a>
 The password that corresponds to the user name\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Username`  <a name="cfn-appflow-connectorprofile-veevaconnectorprofilecredentials-username"></a>
 The name of the user\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-connectorprofile-veevaconnectorprofilecredentials--seealso"></a>
+ [VeevaConnectorProfileCredentials](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_VeevaConnectorProfileCredentials.html) in the *Amazon AppFlow API Reference*\.

