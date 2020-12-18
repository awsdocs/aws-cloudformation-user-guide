# AWS::IoT::DomainConfiguration ServerCertificateSummary<a name="aws-properties-iot-domainconfiguration-servercertificatesummary"></a>

An object that contains information about a server certificate\.

## Syntax<a name="aws-properties-iot-domainconfiguration-servercertificatesummary-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-domainconfiguration-servercertificatesummary-syntax.json"></a>

```
{
  "[ServerCertificateArn](#cfn-iot-domainconfiguration-servercertificatesummary-servercertificatearn)" : String,
  "[ServerCertificateStatus](#cfn-iot-domainconfiguration-servercertificatesummary-servercertificatestatus)" : String,
  "[ServerCertificateStatusDetail](#cfn-iot-domainconfiguration-servercertificatesummary-servercertificatestatusdetail)" : String
}
```

### YAML<a name="aws-properties-iot-domainconfiguration-servercertificatesummary-syntax.yaml"></a>

```
  [ServerCertificateArn](#cfn-iot-domainconfiguration-servercertificatesummary-servercertificatearn): String
  [ServerCertificateStatus](#cfn-iot-domainconfiguration-servercertificatesummary-servercertificatestatus): String
  [ServerCertificateStatusDetail](#cfn-iot-domainconfiguration-servercertificatesummary-servercertificatestatusdetail): String
```

## Properties<a name="aws-properties-iot-domainconfiguration-servercertificatesummary-properties"></a>

`ServerCertificateArn`  <a name="cfn-iot-domainconfiguration-servercertificatesummary-servercertificatearn"></a>
The ARN of the server certificate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerCertificateStatus`  <a name="cfn-iot-domainconfiguration-servercertificatesummary-servercertificatestatus"></a>
The status of the server certificate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerCertificateStatusDetail`  <a name="cfn-iot-domainconfiguration-servercertificatesummary-servercertificatestatusdetail"></a>
Details that explain the status of the server certificate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)