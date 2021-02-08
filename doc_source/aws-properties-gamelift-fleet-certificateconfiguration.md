# AWS::GameLift::Fleet CertificateConfiguration<a name="aws-properties-gamelift-fleet-certificateconfiguration"></a>

Information about the use of a TLS/SSL certificate for a fleet\. TLS certificate generation is enabled at the fleet level, with one certificate generated for the fleet\. When this feature is enabled, the certificate can be retrieved using the GameLift Server SDK call `GetInstanceCertificate`\. All instances in a fleet share the same certificate\. 

## Syntax<a name="aws-properties-gamelift-fleet-certificateconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-gamelift-fleet-certificateconfiguration-syntax.json"></a>

```
{
  "[CertificateType](#cfn-gamelift-fleet-certificateconfiguration-certificatetype)" : String
}
```

### YAML<a name="aws-properties-gamelift-fleet-certificateconfiguration-syntax.yaml"></a>

```
  [CertificateType](#cfn-gamelift-fleet-certificateconfiguration-certificatetype): String
```

## Properties<a name="aws-properties-gamelift-fleet-certificateconfiguration-properties"></a>

`CertificateType`  <a name="cfn-gamelift-fleet-certificateconfiguration-certificatetype"></a>
Indicates whether a TLS/SSL certificate is generated for the fleet\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `DISABLED | GENERATED`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-gamelift-fleet-certificateconfiguration--seealso"></a>
+ [ Create GameLift Resources Using AWS CloudFormation](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+  [Deploy a GameLift Fleet for a Custom Game Build](https://docs.aws.amazon.com/gamelift/latest/developerguide/fleets-creating.html) in the *Amazon GameLift Developer Guide* 
+  [Deploy a Realtime Servers Fleet](https://docs.aws.amazon.com/gamelift/latest/developerguide/realtime-fleets-creating.html) in the *Amazon GameLift Developer Guide* 
+  [CertificateConfiguration](https://docs.aws.amazon.com/gamelift/latest/apireference/API_CertificateConfiguration.html) in the *Amazon GameLift API Reference* 

