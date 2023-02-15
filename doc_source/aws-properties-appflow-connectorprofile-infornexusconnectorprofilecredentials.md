# AWS::AppFlow::ConnectorProfile InforNexusConnectorProfileCredentials<a name="aws-properties-appflow-connectorprofile-infornexusconnectorprofilecredentials"></a>

 The `InforNexusConnectorProfileCredentials` property type specifies the connector\-specific profile credentials required by Infor Nexus\. 

## Syntax<a name="aws-properties-appflow-connectorprofile-infornexusconnectorprofilecredentials-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-connectorprofile-infornexusconnectorprofilecredentials-syntax.json"></a>

```
{
  "[AccessKeyId](#cfn-appflow-connectorprofile-infornexusconnectorprofilecredentials-accesskeyid)" : String,
  "[Datakey](#cfn-appflow-connectorprofile-infornexusconnectorprofilecredentials-datakey)" : String,
  "[SecretAccessKey](#cfn-appflow-connectorprofile-infornexusconnectorprofilecredentials-secretaccesskey)" : String,
  "[UserId](#cfn-appflow-connectorprofile-infornexusconnectorprofilecredentials-userid)" : String
}
```

### YAML<a name="aws-properties-appflow-connectorprofile-infornexusconnectorprofilecredentials-syntax.yaml"></a>

```
  [AccessKeyId](#cfn-appflow-connectorprofile-infornexusconnectorprofilecredentials-accesskeyid): String
  [Datakey](#cfn-appflow-connectorprofile-infornexusconnectorprofilecredentials-datakey): String
  [SecretAccessKey](#cfn-appflow-connectorprofile-infornexusconnectorprofilecredentials-secretaccesskey): String
  [UserId](#cfn-appflow-connectorprofile-infornexusconnectorprofilecredentials-userid): String
```

## Properties<a name="aws-properties-appflow-connectorprofile-infornexusconnectorprofilecredentials-properties"></a>

`AccessKeyId`  <a name="cfn-appflow-connectorprofile-infornexusconnectorprofilecredentials-accesskeyid"></a>
 The Access Key portion of the credentials\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Datakey`  <a name="cfn-appflow-connectorprofile-infornexusconnectorprofilecredentials-datakey"></a>
 The encryption keys used to encrypt data\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretAccessKey`  <a name="cfn-appflow-connectorprofile-infornexusconnectorprofilecredentials-secretaccesskey"></a>
 The secret key used to sign requests\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserId`  <a name="cfn-appflow-connectorprofile-infornexusconnectorprofilecredentials-userid"></a>
 The identifier for the user\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-connectorprofile-infornexusconnectorprofilecredentials--seealso"></a>
+ [InforNexusConnectorProfileCredentials](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_InforNexusConnectorProfileCredentials.html) in the *Amazon AppFlow API Reference*\.

