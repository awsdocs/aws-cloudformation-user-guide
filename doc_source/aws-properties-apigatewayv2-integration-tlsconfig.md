# AWS::ApiGatewayV2::Integration TlsConfig<a name="aws-properties-apigatewayv2-integration-tlsconfig"></a>

The `TlsConfig` property specifies the TLS configuration for a private integration\. If you specify a TLS configuration, private integration traffic uses the HTTPS protocol\. Supported only for HTTP APIs\.

## Syntax<a name="aws-properties-apigatewayv2-integration-tlsconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apigatewayv2-integration-tlsconfig-syntax.json"></a>

```
{
  "[ServerNameToVerify](#cfn-apigatewayv2-integration-tlsconfig-servernametoverify)" : String
}
```

### YAML<a name="aws-properties-apigatewayv2-integration-tlsconfig-syntax.yaml"></a>

```
  [ServerNameToVerify](#cfn-apigatewayv2-integration-tlsconfig-servernametoverify): String
```

## Properties<a name="aws-properties-apigatewayv2-integration-tlsconfig-properties"></a>

`ServerNameToVerify`  <a name="cfn-apigatewayv2-integration-tlsconfig-servernametoverify"></a>
If you specify a server name, API Gateway uses it to verify the hostname on the integration's certificate\. The server name is also included in the TLS handshake to support Server Name Indication \(SNI\) or virtual hosting\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)