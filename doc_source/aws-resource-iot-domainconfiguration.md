# AWS::IoT::DomainConfiguration<a name="aws-resource-iot-domainconfiguration"></a>

Specifies a domain configuration\.

## Syntax<a name="aws-resource-iot-domainconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-domainconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::IoT::DomainConfiguration",
  "Properties" : {
      "[AuthorizerConfig](#cfn-iot-domainconfiguration-authorizerconfig)" : AuthorizerConfig,
      "[DomainConfigurationName](#cfn-iot-domainconfiguration-domainconfigurationname)" : String,
      "[DomainConfigurationStatus](#cfn-iot-domainconfiguration-domainconfigurationstatus)" : String,
      "[DomainName](#cfn-iot-domainconfiguration-domainname)" : String,
      "[ServerCertificateArns](#cfn-iot-domainconfiguration-servercertificatearns)" : [ String, ... ],
      "[ServiceType](#cfn-iot-domainconfiguration-servicetype)" : String,
      "[Tags](#cfn-iot-domainconfiguration-tags)" : Tags,
      "[ValidationCertificateArn](#cfn-iot-domainconfiguration-validationcertificatearn)" : String
    }
}
```

### YAML<a name="aws-resource-iot-domainconfiguration-syntax.yaml"></a>

```
Type: AWS::IoT::DomainConfiguration
Properties: 
  [AuthorizerConfig](#cfn-iot-domainconfiguration-authorizerconfig): 
    AuthorizerConfig
  [DomainConfigurationName](#cfn-iot-domainconfiguration-domainconfigurationname): String
  [DomainConfigurationStatus](#cfn-iot-domainconfiguration-domainconfigurationstatus): String
  [DomainName](#cfn-iot-domainconfiguration-domainname): String
  [ServerCertificateArns](#cfn-iot-domainconfiguration-servercertificatearns): 
    - String
  [ServiceType](#cfn-iot-domainconfiguration-servicetype): String
  [Tags](#cfn-iot-domainconfiguration-tags): 
    Tags
  [ValidationCertificateArn](#cfn-iot-domainconfiguration-validationcertificatearn): String
```

## Properties<a name="aws-resource-iot-domainconfiguration-properties"></a>

`AuthorizerConfig`  <a name="cfn-iot-domainconfiguration-authorizerconfig"></a>
An object that specifies the authorization service for a domain\.  
*Required*: No  
*Type*: [AuthorizerConfig](aws-properties-iot-domainconfiguration-authorizerconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainConfigurationName`  <a name="cfn-iot-domainconfiguration-domainconfigurationname"></a>
The name of the domain configuration\. This value must be unique to a region\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DomainConfigurationStatus`  <a name="cfn-iot-domainconfiguration-domainconfigurationstatus"></a>
The status to which the domain configuration should be updated\.  
Valid values: `ENABLED` \| `DISABLED`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainName`  <a name="cfn-iot-domainconfiguration-domainname"></a>
The name of the domain\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServerCertificateArns`  <a name="cfn-iot-domainconfiguration-servercertificatearns"></a>
The ARNs of the certificates that AWS IoT passes to the device during the TLS handshake\. Currently you can specify only one certificate ARN\. This value is not required for AWS\-managed domains\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServiceType`  <a name="cfn-iot-domainconfiguration-servicetype"></a>
The type of service delivered by the endpoint\.  
AWS IoT Core currently supports only the `DATA` service type\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-iot-domainconfiguration-tags"></a>
Metadata which can be used to manage the domain configuration\.  
For URI Request parameters use format: \.\.\.key1=value1&key2=value2\.\.\.  
For the CLI command\-line parameter use format: &&tags "key1=value1&key2=value2\.\.\."  
For the cli\-input\-json file use format: "tags": "key1=value1&key2=value2\.\.\."
*Required*: No  
*Type*: [Tags](aws-properties-iot-domainconfiguration-tags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValidationCertificateArn`  <a name="cfn-iot-domainconfiguration-validationcertificatearn"></a>
The certificate used to validate the server certificate and prove domain name ownership\. This certificate must be signed by a public certificate authority\. This value is not required for AWS\-managed domains\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-iot-domainconfiguration-return-values"></a>

### Ref<a name="aws-resource-iot-domainconfiguration-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the domain configuration name\. For example:

 `{ "Ref": "MyDomainConfiguration" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-iot-domainconfiguration-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iot-domainconfiguration-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the domain configuration\.

`DomainType`  <a name="DomainType-fn::getatt"></a>
The type of service delivered by the domain\.

`ServerCertificates`  <a name="ServerCertificates-fn::getatt"></a>
The ARNs of the certificates that AWS IoT passes to the device during the TLS handshake\. Currently you can specify only one certificate ARN\. This value is not required for AWS\-managed domains\.