# AWS::PCAConnectorAD::Connector<a name="aws-resource-pcaconnectorad-connector"></a>

Creates a connector between AWS Private CA and an Active Directory\. You must specify the private CA, directory ID, and security groups\.

## Syntax<a name="aws-resource-pcaconnectorad-connector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pcaconnectorad-connector-syntax.json"></a>

```
{
  "Type" : "AWS::PCAConnectorAD::Connector",
  "Properties" : {
      "[CertificateAuthorityArn](#cfn-pcaconnectorad-connector-certificateauthorityarn)" : String,
      "[DirectoryId](#cfn-pcaconnectorad-connector-directoryid)" : String,
      "[Tags](#cfn-pcaconnectorad-connector-tags)" : {Key: Value, ...},
      "[VpcInformation](#cfn-pcaconnectorad-connector-vpcinformation)" : VpcInformation
    }
}
```

### YAML<a name="aws-resource-pcaconnectorad-connector-syntax.yaml"></a>

```
Type: AWS::PCAConnectorAD::Connector
Properties: 
  [CertificateAuthorityArn](#cfn-pcaconnectorad-connector-certificateauthorityarn): String
  [DirectoryId](#cfn-pcaconnectorad-connector-directoryid): String
  [Tags](#cfn-pcaconnectorad-connector-tags): 
    Key: Value
  [VpcInformation](#cfn-pcaconnectorad-connector-vpcinformation): 
    VpcInformation
```

## Properties<a name="aws-resource-pcaconnectorad-connector-properties"></a>

`CertificateAuthorityArn`  <a name="cfn-pcaconnectorad-connector-certificateauthorityarn"></a>
The Amazon Resource Name \(ARN\) of the certificate authority being used\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `5`  
*Maximum*: `200`  
*Pattern*: `arn:[\w-]+:acm-pca:[\w-]+:[0-9]+:certificate-authority\/[0-9a-f]{8}(-[0-9a-f]{4}){3}-[0-9a-f]{12}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DirectoryId`  <a name="cfn-pcaconnectorad-connector-directoryid"></a>
The identifier of the Active Directory\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `d-[0-9a-f]{10}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-pcaconnectorad-connector-tags"></a>
Metadata assigned to a connector consisting of a key\-value pair\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcInformation`  <a name="cfn-pcaconnectorad-connector-vpcinformation"></a>
Information of the VPC and security group\(s\) used with the connector\.  
*Required*: Yes  
*Type*: [VpcInformation](aws-properties-pcaconnectorad-connector-vpcinformation.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-pcaconnectorad-connector-return-values"></a>

### Fn::GetAtt<a name="aws-resource-pcaconnectorad-connector-return-values-fn--getatt"></a>

#### <a name="aws-resource-pcaconnectorad-connector-return-values-fn--getatt-fn--getatt"></a>

`ConnectorArn`  <a name="ConnectorArn-fn::getatt"></a>
 The Amazon Resource Name \(ARN\) that was returned when you called [CreateConnector](https://docs.aws.amazon.com/pca-connector-ad/latest/APIReference/API_CreateConnector.html)\. 