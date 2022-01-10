# AWS::Transfer::Server ProtocolDetails<a name="aws-properties-transfer-server-protocoldetails"></a>

Protocol settings that are configured for your server\.

## Syntax<a name="aws-properties-transfer-server-protocoldetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-transfer-server-protocoldetails-syntax.json"></a>

```
{
  "[PassiveIp](#cfn-transfer-server-protocoldetails-passiveip)" : String,
  "[TlsSessionResumptionMode](#cfn-transfer-server-protocoldetails-tlssessionresumptionmode)" : String
}
```

### YAML<a name="aws-properties-transfer-server-protocoldetails-syntax.yaml"></a>

```
  [PassiveIp](#cfn-transfer-server-protocoldetails-passiveip): String
  [TlsSessionResumptionMode](#cfn-transfer-server-protocoldetails-tlssessionresumptionmode): String
```

## Properties<a name="aws-properties-transfer-server-protocoldetails-properties"></a>

`PassiveIp`  <a name="cfn-transfer-server-protocoldetails-passiveip"></a>
 Indicates passive mode, for FTP and FTPS protocols\. Enter a single dotted\-quad IPv4 address, such as the external IP address of a firewall, router, or load balancer\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TlsSessionResumptionMode`  <a name="cfn-transfer-server-protocoldetails-tlssessionresumptionmode"></a>
A property used with Transfer servers that use the FTPS protocol\. TLS Session Resumption provides a mechanism to resume or share a negotiated secret key between the control and data connection for an FTPS session\. `TlsSessionResumptionMode` determines whether or not the server resumes recent, negotiated sessions through a unique session ID\. This property is available during `CreateServer` and `UpdateServer` calls\. If a `TlsSessionResumptionMode` value is not specified during CreateServer, it is set to `ENFORCED` by default\.  
+  `DISABLED`: the server does not process TLS session resumption client requests and creates a new TLS session for each request\. 
+  `ENABLED`: the server processes and accepts clients that are performing TLS session resumption\. The server doesn't reject client data connections that do not perform the TLS session resumption client processing\.
+  `ENFORCED`: the server processes and accepts clients that are performing TLS session resumption\. The server rejects client data connections that do not perform the TLS session resumption client processing\. Before you set the value to `ENFORCED`, test your clients\.
**Note**  
Not all FTPS clients perform TLS session resumption\. So, if you choose to enforce TLS session resumption, you prevent any connections from FTPS clients that don't perform the protocol negotiation\. To determine whether or not you can use the `ENFORCED` value, you need to test your clients\.
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED | ENFORCED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)