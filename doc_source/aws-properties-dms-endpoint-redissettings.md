# AWS::DMS::Endpoint RedisSettings<a name="aws-properties-dms-endpoint-redissettings"></a>

Provides information that defines a Redis target endpoint\. This information includes the output format of records applied to the endpoint and details of transaction and control table data information\. For information about other available settings, see [ Specifying endpoint settings for Redis as a target](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.Redis.html#CHAP_Target.Redis.EndpointSettings) in the *AWS Database Migration Service User Guide*\.

## Syntax<a name="aws-properties-dms-endpoint-redissettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dms-endpoint-redissettings-syntax.json"></a>

```
{
  "[AuthPassword](#cfn-dms-endpoint-redissettings-authpassword)" : String,
  "[AuthType](#cfn-dms-endpoint-redissettings-authtype)" : String,
  "[AuthUserName](#cfn-dms-endpoint-redissettings-authusername)" : String,
  "[Port](#cfn-dms-endpoint-redissettings-port)" : Double,
  "[ServerName](#cfn-dms-endpoint-redissettings-servername)" : String,
  "[SslCaCertificateArn](#cfn-dms-endpoint-redissettings-sslcacertificatearn)" : String,
  "[SslSecurityProtocol](#cfn-dms-endpoint-redissettings-sslsecurityprotocol)" : String
}
```

### YAML<a name="aws-properties-dms-endpoint-redissettings-syntax.yaml"></a>

```
  [AuthPassword](#cfn-dms-endpoint-redissettings-authpassword): String
  [AuthType](#cfn-dms-endpoint-redissettings-authtype): String
  [AuthUserName](#cfn-dms-endpoint-redissettings-authusername): String
  [Port](#cfn-dms-endpoint-redissettings-port): Double
  [ServerName](#cfn-dms-endpoint-redissettings-servername): String
  [SslCaCertificateArn](#cfn-dms-endpoint-redissettings-sslcacertificatearn): String
  [SslSecurityProtocol](#cfn-dms-endpoint-redissettings-sslsecurityprotocol): String
```

## Properties<a name="aws-properties-dms-endpoint-redissettings-properties"></a>

`AuthPassword`  <a name="cfn-dms-endpoint-redissettings-authpassword"></a>
The password provided with the `auth-role` and `auth-token` options of the `AuthType` setting for a Redis target endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthType`  <a name="cfn-dms-endpoint-redissettings-authtype"></a>
The type of authentication to perform when connecting to a Redis target\. Options include `none`, `auth-token`, and `auth-role`\. The `auth-token` option requires an `AuthPassword` value to be provided\. The `auth-role` option requires `AuthUserName` and `AuthPassword` values to be provided\.  
*Required*: No  
*Type*: String  
*Allowed values*: `auth-role | auth-token | none`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthUserName`  <a name="cfn-dms-endpoint-redissettings-authusername"></a>
The user name provided with the `auth-role` option of the `AuthType` setting for a Redis target endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-dms-endpoint-redissettings-port"></a>
Transmission Control Protocol \(TCP\) port for the endpoint\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerName`  <a name="cfn-dms-endpoint-redissettings-servername"></a>
Fully qualified domain name of the endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SslCaCertificateArn`  <a name="cfn-dms-endpoint-redissettings-sslcacertificatearn"></a>
The Amazon Resource Name \(ARN\) for the certificate authority \(CA\) that DMS uses to connect to your Redis target endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SslSecurityProtocol`  <a name="cfn-dms-endpoint-redissettings-sslsecurityprotocol"></a>
The connection to a Redis target endpoint using Transport Layer Security \(TLS\)\. Valid values include `plaintext` and `ssl-encryption`\. The default is `ssl-encryption`\. The `ssl-encryption` option makes an encrypted connection\. Optionally, you can identify an Amazon Resource Name \(ARN\) for an SSL certificate authority \(CA\) using the `SslCaCertificateArn `setting\. If an ARN isn't given for a CA, DMS uses the Amazon root CA\.  
The `plaintext` option doesn't provide Transport Layer Security \(TLS\) encryption for traffic between endpoint and database\.  
*Required*: No  
*Type*: String  
*Allowed values*: `plaintext | ssl-encryption`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)