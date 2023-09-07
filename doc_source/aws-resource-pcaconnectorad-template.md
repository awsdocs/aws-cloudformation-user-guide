# AWS::PCAConnectorAD::Template<a name="aws-resource-pcaconnectorad-template"></a>

Creates an Active Directory compatible certificate template\. The connectors issues certificates using these templates based on the requester’s Active Directory group membership\.

## Syntax<a name="aws-resource-pcaconnectorad-template-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pcaconnectorad-template-syntax.json"></a>

```
{
  "Type" : "AWS::PCAConnectorAD::Template",
  "Properties" : {
      "[ConnectorArn](#cfn-pcaconnectorad-template-connectorarn)" : String,
      "[Definition](#cfn-pcaconnectorad-template-definition)" : TemplateDefinition,
      "[Name](#cfn-pcaconnectorad-template-name)" : String,
      "[ReenrollAllCertificateHolders](#cfn-pcaconnectorad-template-reenrollallcertificateholders)" : Boolean,
      "[Tags](#cfn-pcaconnectorad-template-tags)" : {Key: Value, ...}
    }
}
```

### YAML<a name="aws-resource-pcaconnectorad-template-syntax.yaml"></a>

```
Type: AWS::PCAConnectorAD::Template
Properties: 
  [ConnectorArn](#cfn-pcaconnectorad-template-connectorarn): String
  [Definition](#cfn-pcaconnectorad-template-definition): 
    TemplateDefinition
  [Name](#cfn-pcaconnectorad-template-name): String
  [ReenrollAllCertificateHolders](#cfn-pcaconnectorad-template-reenrollallcertificateholders): Boolean
  [Tags](#cfn-pcaconnectorad-template-tags): 
    Key: Value
```

## Properties<a name="aws-resource-pcaconnectorad-template-properties"></a>

`ConnectorArn`  <a name="cfn-pcaconnectorad-template-connectorarn"></a>
 The Amazon Resource Name \(ARN\) that was returned when you called [CreateConnector](https://docs.aws.amazon.com/pca-connector-ad/latest/APIReference/API_CreateConnector.html)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `5`  
*Maximum*: `200`  
*Pattern*: `arn:[\w-]+:pca-connector-ad:[\w-]+:[0-9]+:connector\/[0-9a-f]{8}(-[0-9a-f]{4}){3}-[0-9a-f]{12}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Definition`  <a name="cfn-pcaconnectorad-template-definition"></a>
Template configuration to define the information included in certificates\. Define certificate validity and renewal periods, certificate request handling and enrollment options, key usage extensions, application policies, and cryptography settings\.  
*Required*: Yes  
*Type*: [TemplateDefinition](aws-properties-pcaconnectorad-template-templatedefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-pcaconnectorad-template-name"></a>
Name of the templates\. Template names must be unique\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `(?!^\s+$)((?![\x5c'\x2b,;<=>#\x22])([\x20-\x7E]))+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReenrollAllCertificateHolders`  <a name="cfn-pcaconnectorad-template-reenrollallcertificateholders"></a>
This setting allows the major version of a template to be increased automatically\. All members of Active Directory groups that are allowed to enroll with a template will receive a new certificate issued using that template\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-pcaconnectorad-template-tags"></a>
Metadata assigned to a template consisting of a key\-value pair\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-pcaconnectorad-template-return-values"></a>

### Ref<a name="aws-resource-pcaconnectorad-template-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-pcaconnectorad-template-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-pcaconnectorad-template-return-values-fn--getatt-fn--getatt"></a>

`TemplateArn`  <a name="TemplateArn-fn::getatt"></a>
 The Amazon Resource Name \(ARN\) that was returned when you called [CreateTemplate](https://docs.aws.amazon.com/pca-connector-ad/latest/APIReference/API_CreateTemplate.html) \. 