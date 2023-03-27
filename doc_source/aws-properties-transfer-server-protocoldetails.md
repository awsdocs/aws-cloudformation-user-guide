# AWS::Transfer::Server ProtocolDetails<a name="aws-properties-transfer-server-protocoldetails"></a>

Protocol settings that are configured for your server\.

## Syntax<a name="aws-properties-transfer-server-protocoldetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-transfer-server-protocoldetails-syntax.json"></a>

```
{
  "[As2Transports](#cfn-transfer-server-protocoldetails-as2transports)" : [ As2Transport, ... ],
  "[PassiveIp](#cfn-transfer-server-protocoldetails-passiveip)" : String,
  "[SetStatOption](#cfn-transfer-server-protocoldetails-setstatoption)" : String,
  "[TlsSessionResumptionMode](#cfn-transfer-server-protocoldetails-tlssessionresumptionmode)" : String
}
```

### YAML<a name="aws-properties-transfer-server-protocoldetails-syntax.yaml"></a>

```
  [As2Transports](#cfn-transfer-server-protocoldetails-as2transports): 
    - As2Transport
  [PassiveIp](#cfn-transfer-server-protocoldetails-passiveip): String
  [SetStatOption](#cfn-transfer-server-protocoldetails-setstatoption): String
  [TlsSessionResumptionMode](#cfn-transfer-server-protocoldetails-tlssessionresumptionmode): String
```

## Properties<a name="aws-properties-transfer-server-protocoldetails-properties"></a>

`As2Transports`  <a name="cfn-transfer-server-protocoldetails-as2transports"></a>
List of `As2Transport` objects\.  
*Required*: No  
*Type*: List of [As2Transport](aws-properties-transfer-server-as2transport.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PassiveIp`  <a name="cfn-transfer-server-protocoldetails-passiveip"></a>
 Indicates passive mode, for FTP and FTPS protocols\. Enter a single IPv4 address, such as the public IP address of a firewall, router, or load balancer\. For example:   
 `aws transfer update-server --protocol-details PassiveIp=0.0.0.0`   
Replace `0.0.0.0` in the example above with the actual IP address you want to use\.  
 If you change the `PassiveIp` value, you must stop and then restart your Transfer Family server for the change to take effect\. For details on using passive mode \(PASV\) in a NAT environment, see [Configuring your FTPS server behind a firewall or NAT with AWS Transfer Family](http://aws.amazon.com/blogs/storage/configuring-your-ftps-server-behind-a-firewall-or-nat-with-aws-transfer-family/)\. 
 *Special values*   
The `AUTO` and `0.0.0.0` are special values for the `PassiveIp` parameter\. The value `PassiveIp=AUTO` is assigned by default to FTP and FTPS type servers\. In this case, the server automatically responds with one of the endpoint IPs within the PASV response\. `PassiveIp=0.0.0.0` has a more unique application for its usage\. For example, if you have a High Availability \(HA\) Network Load Balancer \(NLB\) environment, where you have 3 subnets, you can only specify a single IP address using the `PassiveIp` parameter\. This reduces the effectiveness of having High Availability\. In this case, you can specify `PassiveIp=0.0.0.0`\. This tells the client to use the same IP address as the Control connection and utilize all AZs for their connections\. Note, however, that not all FTP clients support the `PassiveIp=0.0.0.0` response\. FileZilla and WinSCP do support it\. If you are using other clients, check to see if your client supports the `PassiveIp=0.0.0.0` response\.  
*Required*: No  
*Type*: String  
*Maximum*: `15`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SetStatOption`  <a name="cfn-transfer-server-protocoldetails-setstatoption"></a>
Use the `SetStatOption` to ignore the error that is generated when the client attempts to use `SETSTAT` on a file you are uploading to an S3 bucket\.  
Some SFTP file transfer clients can attempt to change the attributes of remote files, including timestamp and permissions, using commands, such as `SETSTAT` when uploading the file\. However, these commands are not compatible with object storage systems, such as Amazon S3\. Due to this incompatibility, file uploads from these clients can result in errors even when the file is otherwise successfully uploaded\.  
Set the value to `ENABLE_NO_OP` to have the Transfer Family server ignore the `SETSTAT` command, and upload files without needing to make any changes to your SFTP client\. While the `SetStatOption` `ENABLE_NO_OP` setting ignores the error, it does generate a log entry in Amazon CloudWatch Logs, so you can determine when the client is making a `SETSTAT` call\.  
If you want to preserve the original timestamp for your file, and modify other file attributes using `SETSTAT`, you can use Amazon EFS as backend storage with Transfer Family\.
*Required*: No  
*Type*: String  
*Allowed values*: `DEFAULT | ENABLE_NO_OP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TlsSessionResumptionMode`  <a name="cfn-transfer-server-protocoldetails-tlssessionresumptionmode"></a>
A property used with Transfer Family servers that use the FTPS protocol\. TLS Session Resumption provides a mechanism to resume or share a negotiated secret key between the control and data connection for an FTPS session\. `TlsSessionResumptionMode` determines whether or not the server resumes recent, negotiated sessions through a unique session ID\. This property is available during `CreateServer` and `UpdateServer` calls\. If a `TlsSessionResumptionMode` value is not specified during `CreateServer`, it is set to `ENFORCED` by default\.  
+  `DISABLED`: the server does not process TLS session resumption client requests and creates a new TLS session for each request\. 
+  `ENABLED`: the server processes and accepts clients that are performing TLS session resumption\. The server doesn't reject client data connections that do not perform the TLS session resumption client processing\.
+  `ENFORCED`: the server processes and accepts clients that are performing TLS session resumption\. The server rejects client data connections that do not perform the TLS session resumption client processing\. Before you set the value to `ENFORCED`, test your clients\.
**Note**  
Not all FTPS clients perform TLS session resumption\. So, if you choose to enforce TLS session resumption, you prevent any connections from FTPS clients that don't perform the protocol negotiation\. To determine whether or not you can use the `ENFORCED` value, you need to test your clients\.
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED | ENFORCED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)