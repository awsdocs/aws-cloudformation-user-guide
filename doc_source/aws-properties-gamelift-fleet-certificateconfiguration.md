# AWS::GameLift::Fleet CertificateConfiguration<a name="aws-properties-gamelift-fleet-certificateconfiguration"></a>

Determines whether a TLS/SSL certificate is generated for a fleet\. This feature must be enabled when creating the fleet\. All instances in a fleet share the same certificate\. The certificate can be retrieved by calling the [GameLift Server SDK](https://docs.aws.amazon.com/gamelift/latest/developerguide/reference-serversdk.html) operation `GetInstanceCertificate`\. 

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
Indicates whether a TLS/SSL certificate is generated for a fleet\.   
Valid values include:   
+  **GENERATED** \- Generate a TLS/SSL certificate for this fleet\.
+  **DISABLED** \- \(default\) Do not generate a TLS/SSL certificate for this fleet\. 
*Required*: Yes  
*Type*: String  
*Allowed values*: `DISABLED | GENERATED`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-gamelift-fleet-certificateconfiguration--seealso"></a>
+ [ Create GameLift resources using Amazon CloudFront](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+  [Deploy a GameLift fleet for a custom game build](https://docs.aws.amazon.com/gamelift/latest/developerguide/fleets-creating.html) in the *Amazon GameLift Developer Guide* 
+  [Deploy a Realtime Servers fleet](https://docs.aws.amazon.com/gamelift/latest/developerguide/realtime-fleets-creating.html) in the *Amazon GameLift Developer Guide* 
+  [CertificateConfiguration](https://docs.aws.amazon.com/gamelift/latest/apireference/API_CertificateConfiguration.html) in the *Amazon GameLift API Reference* 

