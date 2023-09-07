# AWS::PCAConnectorAD::ServicePrincipalName<a name="aws-resource-pcaconnectorad-serviceprincipalname"></a>

Creates a service principal name \(SPN\) for the service account in Active Directory\. Kerberos authentication uses SPNs to associate a service instance with a service sign\-in account\.

## Syntax<a name="aws-resource-pcaconnectorad-serviceprincipalname-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pcaconnectorad-serviceprincipalname-syntax.json"></a>

```
{
  "Type" : "AWS::PCAConnectorAD::ServicePrincipalName",
  "Properties" : {
      "[ConnectorArn](#cfn-pcaconnectorad-serviceprincipalname-connectorarn)" : String,
      "[DirectoryRegistrationArn](#cfn-pcaconnectorad-serviceprincipalname-directoryregistrationarn)" : String
    }
}
```

### YAML<a name="aws-resource-pcaconnectorad-serviceprincipalname-syntax.yaml"></a>

```
Type: AWS::PCAConnectorAD::ServicePrincipalName
Properties: 
  [ConnectorArn](#cfn-pcaconnectorad-serviceprincipalname-connectorarn): String
  [DirectoryRegistrationArn](#cfn-pcaconnectorad-serviceprincipalname-directoryregistrationarn): String
```

## Properties<a name="aws-resource-pcaconnectorad-serviceprincipalname-properties"></a>

`ConnectorArn`  <a name="cfn-pcaconnectorad-serviceprincipalname-connectorarn"></a>
The Amazon Resource Name \(ARN\) that was returned when you called [CreateConnector\.html](https://docs.aws.amazon.com/pca-connector-ad/latest/APIReference/API_CreateConnector.html)\.  
*Required*: No  
*Type*: String  
*Minimum*: `5`  
*Maximum*: `200`  
*Pattern*: `arn:[\w-]+:pca-connector-ad:[\w-]+:[0-9]+:connector\/[0-9a-f]{8}(-[0-9a-f]{4}){3}-[0-9a-f]{12}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DirectoryRegistrationArn`  <a name="cfn-pcaconnectorad-serviceprincipalname-directoryregistrationarn"></a>
The Amazon Resource Name \(ARN\) that was returned when you called [CreateDirectoryRegistration](https://docs.aws.amazon.com/pca-connector-ad/latest/APIReference/API_CreateDirectoryRegistration.html)\.  
*Required*: No  
*Type*: String  
*Minimum*: `5`  
*Maximum*: `200`  
*Pattern*: `arn:[\w-]+:pca-connector-ad:[\w-]+:[0-9]+:directory-registration\/d-[0-9a-f]{10}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)